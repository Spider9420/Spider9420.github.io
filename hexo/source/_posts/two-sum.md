---
title: two sum
catalog: true
date: 2019-07-10 14:49:17
subtitle: "Array test"
header-img:  "/source/_posts/two-sum/君.jpg"
tags: LeetCode
---
## Problem
Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.
## Example
Given nums = [2, 7, 11, 15], target = 9,
Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
## Solution
```
class Solution {
public int[] twoSum(int[] nums, int target) {
int n=nums.length;
int[] arr=new int[2];
loop:for(int i=0;i<n;i++){
for(int j=i+1;j<n;j++){
if(nums[j]==target-nums[i]){
arr[0]=i;
arr[1]=j;
break loop;
}
}
}
return arr;               
}
}
```


