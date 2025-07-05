# 4. Median of Two Sorted Arrays

**Difficulty:** Hard  
**Language:** C++  

#### *Problem Link*: [4. Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)

## Performance
- **Runtime:** 5 ms (beats 14.01%)
- **Memory:** 96.04 MB (beats 10.24%)

## Solution
```cpp
class Solution {
public:
    double findMedianSortedArrays(vector<int>& nums1, vector<int>& nums2) {
        std::vector<int> nums;
        for(auto n: nums1)
            nums.push_back(n);
        for(auto n: nums2)
            nums.push_back(n);
        std::sort(nums.begin(), nums.end());
        double m{0};
        if(!nums.empty())
        {
            if(nums.size() % 2 == 0) {
                double d1 = nums[nums.size() / 2 - 1]; 
                double d2 = nums[nums.size() / 2];
                m = (d1 + d2)/2;       
            } else 
                m = nums[nums.size() / 2];
        }
        return m;
        
    }
};
```

## Complexity Analysis

Time Complexity: O(n log n)
Space Complexity: O(1)

> ⚠️ _This complexity was estimated locally. Review advised._



---
*Solution automatically synced by [GitSync](https://github.com/pramay88/GitSync) 🚀*
