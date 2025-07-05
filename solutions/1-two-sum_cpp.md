# 1. Two Sum

**Difficulty:** Easy  
**Language:** C++  

#### *Problem Link*: [1. Two Sum](https://leetcode.com/problems/two-sum/)

## Performance
- **Runtime:** 1 ms (beats 80.26%)
- **Memory:** 14.76 MB (beats 51.22%)

## Solution
```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
       unordered_map<int, int> mp;
        for (int i = 0; i < nums.size(); i++) {
            if (mp.find(target - nums[i]) != mp.end()) {
                return {mp[target - nums[i]], i};
            }
            mp[nums[i]] = i;
        }
        return {};
    }
};
```

## Complexity Analysis

Time Complexity: O(n)
Space Complexity: O(1)

> ⚠️ _This complexity was estimated locally. Review advised._



---
*Solution automatically synced by [GitSync](https://github.com/pramay88/GitSync) 🚀*
