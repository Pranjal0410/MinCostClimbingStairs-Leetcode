

# Min Cost Climbing Stairs (LeetCode Problem #746)

## Problem Description

You are given an array `cost` where `cost[i]` is the cost of `i-th` step on a staircase. You can start climbing from either the first step or the second step. You can either climb one or two steps at a time. 

Return the minimum cost to reach the top of the floor.

### Example

```plaintext
Input: cost = [10, 15, 20]
Output: 15
Explanation: Cheapest is to start on cost[1], pay that cost, and go to the top.
```

## Solution

The problem can be efficiently solved using dynamic programming. We can define an array `dp` where `dp[i]` represents the minimum cost to reach step `i`.

The recurrence relation is:

```python
dp[i] = cost[i] + min(dp[i-1], dp[i-2])
```

We iterate through the steps, and at each step, we take the minimum of the cost to reach the previous step and the step before that.

## Complexity Analysis

The time complexity of this solution is O(n) where n is the length of the `cost` array.

## Usage

You can copy the solution code and use it in your project. You can modify the `minCostClimbingStairs` function to accept different inputs if necessary.

```python
def minCostClimbingStairs(cost):
    # Implementation of the solution here

# Example Usage
cost = [10, 15, 20]
result = minCostClimbingStairs(cost)
print(result)  # Output: 15
```

## Contributing

If you have a better solution or any improvements, feel free to contribute!
