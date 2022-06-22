## 704 Binary Search
```
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        for i in range(len(nums)):
            if nums[i]==target:
                return i
        if i==len(nums)-1:
            return -1
```
```
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        left, right=0, len(nums)-1
        while left<=right:
            middle=(left+right)//2
            if target<nums[middle]:
                right=middle-1
            elif target>nums[middle]:
                left=middle+1
            else:
                return middle
        return -1
```
