# Bitwise-XOR-of-All-Pairings

You are given two 0-indexed arrays, nums1 and nums2, consisting of non-negative integers. There exists another array, nums3, which contains the bitwise XOR of all pairings of integers between nums1 and nums2 (every integer in nums1 is paired with every integer in nums2 exactly once).

Return the bitwise XOR of all integers in nums3.

class Solution:
    def xorAllNums(self, nums1: List[int], nums2: List[int]) -> int:
        return (len(nums2)%2*reduce(ixor, nums1))^(len(nums1)%2*reduce(ixor, nums2))
        
