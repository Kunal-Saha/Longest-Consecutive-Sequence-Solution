```
# Longest-Consecutive-Sequence-Solution
class Solution {
public:
    int longestConsecutive(vector<int>& nums) {
      int maxi=0;
        set<int>s;
        for(int x:nums)
        {
            s.insert(x);
        }
        for(int x:nums)
        {
            if(!s.count(x-1))
            {
                int curr=x;
                int ans=1;
                while(s.count(curr+1))
                {
                    curr+=1;
                    ans+=1;
                }
                maxi=max(maxi,ans);
            }
        }
        return maxi;
    }
};
```
