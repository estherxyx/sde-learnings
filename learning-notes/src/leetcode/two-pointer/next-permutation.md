[leetcode](https://leetcode.cn/problems/next-permutation)
```python
class Solution:
    def nextPermutation(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        i = len(nums)-2
        while i >0 and nums[i] >=nums[i+1]:
            i -= 1
        if i >=0:
            j = len(nums)-1
            while j >0 and nums[i] >nums[j]:
                j -= 1
            nums[i], nums[j] = nums[j],nums[i]
        left = i+1
        right = len(nums)-1
        while left <right:
            nums[left],nums[right] = nums[right] ,nums[left]
            right -= 1
            left -= 1
```

