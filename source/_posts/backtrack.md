---
title: 回溯
tags: interview
date: 2022-08-12 08:55:40
updated: 2022-08-12 08:55:40
categories:
keywords:
---
#### 回溯

1. 识别状态（结束状态，传递状态）
2. 画出状态空间树
3. 在状态树上回溯

时间复杂度：n！

状态：

* 什么状态下，应该返回
* 什么状态下，应该继续回溯，或者剪枝

**Leetcode列表**

* [46. 全排列](https://leetcode.cn/problems/permutations/)
* [47. 全排列 II](https://leetcode.cn/problems/permutations-ii/)

* [17. 电话号码的字母组合](https://leetcode.cn/problems/letter-combinations-of-a-phone-number/)
* [139. 单词拆分](https://leetcode.cn/problems/word-break/)

* [91. 解码方法](https://leetcode.cn/problems/decode-ways/)
* [131. 分割回文串](https://leetcode.cn/problems/palindrome-partitioning/)

* [39. 组合总和](https://leetcode.cn/problems/combination-sum/)
* [78. 子集](https://leetcode.cn/problems/subsets/)

```
 function dfs(node, state):
     if state is a solution:
         report(state) # e.g. add state to final result list
         return
 
     for child in children:
         if child is a part of a potential solution:
             state.add(child) # make move
             dfs(child, state)
             state.remove(child) # backtrack
```
