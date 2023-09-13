# leet-day61

# Candy Distribution

This C++ solution solves the problem of distributing candies to children based on their ratings with the objective of minimizing the total number of candies used. The rules for candy distribution are as follows:

1. Each child must have at least one candy.
2. Children with a higher rating should receive more candies than their neighbors.

The goal is to find the minimum number of candies needed to satisfy these conditions for all children.

## Problem Description

You are given an integer array `ratings`, where `ratings[i]` represents the rating of the `i-th` child. You need to distribute candies to these children based on the rules mentioned above.

### Example

Input: `ratings = [1,0,2]`
Output: `5`
Explanation: You can allocate candies to the first, second, and third child with 2, 1, and 2 candies respectively.

### Constraints

- `n == ratings.length` (Number of children)
- `1 <= n <= 2 * 10^4`
- `0 <= ratings[i] <= 2 * 10^4`

## Approach

1. Initialize a vector `candies` of size `n`, where each element is initially set to 1. This represents that each child starts with at least one candy.

2. Traverse through the `ratings` array from left to right to ensure that higher-rated children receive more candies than their left neighbors. If the rating of a child is greater than the rating of the previous child, increment their candy count by 1.

3. Traverse through the `ratings` array from right to left to ensure that higher-rated children receive more candies than their right neighbors. If the rating of a child is greater than the rating of the next child, update their candy count to be the maximum of their current candy count and one more than the next child's candy count.

4. Calculate the total number of candies needed by summing up the values in the `candies` vector.

5. Return the total number of candies as the minimum number required to satisfy the given conditions.

## Usage

You can use the `candy` function to find the minimum number of candies required for any given set of ratings. Here's how you can use it:

```cpp
Solution solution;
std::vector<int> ratings = {1, 0, 2};
int result = solution.candy(ratings); // Should return 5
```

## Complexity Analysis

- Time Complexity: O(n), where n is the number of children. The algorithm iterates through the `ratings` array twice, once from left to right and once from right to left.
- Space Complexity: O(n) for the `candies` vector, which stores the number of candies for each child.
