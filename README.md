#  LeetCode 1929: Concatenation of Array

##  Problem Statement
Given an integer array `nums` of length `n`, you want to create an array `ans` of length `2n` where `ans` is the concatenation of two `nums` arrays [LeetCode #1929](https://leetcode.com).

**Rules:**
- `ans[i] == nums[i]`
- `ans[i + n] == nums[i]`
- for $0 \le i < n$ (0-indexed).

##  Intuition & Approach
The most efficient way to build the result array is to iterate through the target size ($2n$) and use the **modulo operator (%)** to "wrap around" the original array.

### My Logic:
1. Initialize a new array `ans` with double the length of the input.
2. Loop through every index from `0` to `2n - 1`.
3. Use `i % n` to ensure that when `i` reaches `n`, it resets to index `0` of the input array.
   - *Example:* If `n=3`, then at `i=3`, `3 % 3 = 0`. At `i=4`, `4 % 3 = 1`.

