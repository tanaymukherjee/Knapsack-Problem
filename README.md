# Knapsack-Problem
Implementation of knapsack problem in Python

The knapsack problem is a problem in combinatorial optimization: Given a set of items, each with a weight and a value, determine the number of each item to include in a collection so that the total weight is less than or equal to a given limit and the total value is as large as possible. It derives its name from the problem faced by someone who is constrained by a fixed-size knapsack and must fill it with the most valuable items. The problem often arises in resource allocation where the decision makers have to choose from a set of non-divisible projects or tasks under a fixed budget or time constraint, respectively.

- Problem Description
In the 0-1 knapsack problem, we are given a set of n items. For each item i, it has a value v(i) and a weight w(i) where 1 <= i <= n. We are given a maximum weight W. The problem is to find a collection of items such that the total weight does not exceed W and the total value is maximized. A collection of items means a subset of the set of all items. Thus, an item can either be included just once or not included.

- Problem Solution
1. The function knapsack is defined.
2. It takes three arguments: two lists value and weight; and a number capacity.
3. It returns the maximum value of items that doesn’t exceed capacity in weight.
4. The function creates a table m where m[i][w] will store the maximum value that can be attained with a maximum capacity of w and using only the first i items.
5. It calls knapsack_helper on m with i=n and w=capacity and returns its return value.
6. The function knapsack_helper takes 5 arguments: two lists value and weight; two numbers i and w; and a table m.
7. It returns the maximum value that can be attained using only the first i items while keeping their total weight not more than w.
8. If m[i][w] was already computed before, this value is immediately returned.
9. If i = 0, then 0 is returned.
10. If weight[i] > w, then m[i][w] is set to m[i – 1][w].
11. Otherwise, m[i][w] = (m[i – 1][w – weight[i]] + value[i]) or m[i][w] = m[i – 1][w], whichever is larger.
12. The above computations are done by recursively calling knapsack_helper.

- Reference:
https://en.wikipedia.org/wiki/Knapsack_problem
SanFoundry
