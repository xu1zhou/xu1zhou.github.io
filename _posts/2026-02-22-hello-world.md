---
title: "sliding window"
date: 2026-02-22 20:00:00 +0000
categories: [Blog, Personal]
tags: [intro, first-post]
---


---

## 套路

for 循环套 while循环

---

## [1/11] leetcode 3 thought process

双指针围成window

循环字符长度的right 左指针left hash table 保证可以发现重复字符  
max(res,cur)

return res

难点:

example : abcc  
当发现重复字符时c,这个字符重复的可能是刚加入进hash table的c,此时要左移左指针到前一个c才能去掉重复的c  

example : abca  
当a为重复字符,左移一位遍可消除重复字符

所以消除字符的过程是一个以hash表不再重负重复为结束条件的while循环

---

## [2/11] leetcode 3090

---

## [3/11] leetcode 1493

删除1个0后有最长的连续1子串,条件转化为窗口里只有一个0的最长子串. 其他逻辑同上

hash table increase right count 0  
if num of 0 > 1  
left point move forward to decrease the 0.

---

## [4/11] leetcode 3634

先排序,让窗口变化对逼近边界条件有意义  

最大元素小于等于最小元素K倍  
Max element <= minimal * K  

一个问题是:  
从左扩大窗口当第一次满足条件就是 minimal removal,还有必要向右移动吗?(不是这样的,最右也是要移动的)

---

## [5/11] leetcode 1208

首先看懂题  

Changing the ith character of s to ith character of t costs |s[i] - t[i]| (i.e., the absolute difference between the ASCII values of the characters).

同位置字母替换,cost是 difference between ASCII values

---

## [6/11] leetcode 904

好吧,其实还是看懂题  

The trees are represented by an integer array fruits where fruits[i] is the type of fruit the ith tree produces.

其实就是只能支持两种类型的,当遇到第三种类型,就要缩小左边边界

---

## [7/11] leetcode 1695

subarray contain unique element  
所有元素都不一样  

当hash table >1 ,缩小左边界  

return max(sum最大值)

---

## [8/11] lt 2958

解法基本一致  

hash表 不超过k次出现

---

## [9/11] lt 2024

复杂一些,因为有两种情况,两种情况都要计算,取最大值  

右边界 for循环  

对每一个元素,看有没有超过k个可替换元素  

如超过,缩小左边界

---

## [10/11] lt 1004

是9的简单版本,只有0-》1

---

## [11/11] lt

---

## 进阶

2730. 找到最长的半重复子字符串  
非暴力做法  

2779. 数组的最大美丽值  

1638  

1658. 将 x 减到 0 的最小操作数  

1817  

1838. 最高频元素的频数  

1876  

2516. 每种字符至少取 K 个  

1948  

2831. 找出最长等值子数组  

1976  

2271. 毯子覆盖的最多白色砖块数  

2022  

2106. 摘水果  

2062  

2555. 两个线段获得的最多奖品  

2081  

2009. 使数组连续的最少操作数  

2084  

1610. 可见点的最大数目  

2147  

2781. 最长合法子字符串的长度  

2204  

3411. 最长乘积等价子数组 非暴力做法约  

2300  

3413. 收集连续 K 个袋子可以获得的最多硬币数量  

2374  

395. 至少有 K 个重复字符的最长子串  

1763. 最长的美好子字符串 非暴力做法  

2968. 执行操作使频率分数最大  

2444  

1040. 移动石子直到连续 II  

2456  

487. 最大连续 1 的个数 II（会员题）  

159. 至多包含两个不同字符的最长子串（会员题）  

340. 至多包含 K 个不同字符的最长子串（会员题）
