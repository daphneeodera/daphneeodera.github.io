---
title: "LeetCode 001: Two Sum"
date: 2025-12-29
categories: [LeetCode, Algorithm]
tags: [Array, HashMap]
---

## Problem Description

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.

## Solution

Use a hash map to store visited numbers and their indices.

```python
def two_sum(nums, target):
    hashmap = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in hashmap:
            return [hashmap[complement], i]
        hashmap[num] = i
```

- **Time complexity:** O(n)  
- **Space complexity:** O(n)
