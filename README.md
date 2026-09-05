# LeetCode 112 - Path Sum

## Problem

Given the root of a binary tree and an integer `targetSum`, determine whether the tree has a **root-to-leaf path** such that adding all the node values along that path gives exactly `targetSum`.

A leaf is a node that has no left or right child.

## Example 1

### Input

```text
root = [5,4,8,11,null,13,4,7,2,null,null,null,1]
targetSum = 22
```

### Output

```text
true
```

### Explanation

The tree contains the following path:

```text
5 → 4 → 11 → 2
```

The sum is:

```text
5 + 4 + 11 + 2 = 22
```

Therefore, the result is `true`.

## Example 2

### Input

```text
root = [1,2,3]
targetSum = 5
```

### Output

```text
false
```

There is no root-to-leaf path whose sum is `5`.

## Approach

This problem can be solved using **Depth-First Search (DFS)** and recursion.

At each node, subtract its value from `targetSum`. Then recursively search the left and right subtrees using the remaining sum.

When a leaf node is reached, check whether its value is equal to the remaining target sum.

## Algorithm

1. If the tree is empty, return `False`.
2. Check whether the current node is a leaf.
3. If it is a leaf, compare its value with `targetSum`.
4. Subtract the current node's value from `targetSum`.
5. Recursively check the left subtree.
6. Recursively check the right subtree.
7. Return `True` if either subtree contains a valid path.

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(h)`

Each node is visited at most once. The recursion stack requires space proportional to the height of the tree.

## LeetCode Details

**Problem Number:** 112
**Problem Name:** Path Sum
**Difficulty:** Easy
**Topics:** Binary Tree, Depth-First Search, Recursion

## Language

Python 3

## File

`solution.py`

## Author

T.Nandhini
