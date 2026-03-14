---
title: "sliding window"
date: 2026-02-22 20:00:00 +0000
categories: [Blog, Personal]
tags: [intro, first-post]
---
fixed length sliding window

non-fixed length sliding window
3. 无重复字符的最长子串 
3090. 每个字符最多出现两次的最长子字符串 1329 同3
1493. 删掉一个元素以后全为 1 的最长子数组 1423
3634. 使数组平衡的最少移除数目 1453
1208. 尽可能使字符串相等 1497
904. 水果成篮 1516
1695. 删除子数组的最大得分 1529
2958. 最多 K 个重复元素的最长子数组 1535
2024. 考试的最大困扰度 1643
1004. 最大连续 1 的个数 III 1656
3641. 最长半重复子数组（会员题）

套路:
for 循环套 while循环

[1/11]leetcode 3
thought process:
双指针围成window

循环字符长度的right
左指针left
hash table 保证可以发现重复字符
max(res,cur)

return res

难点:
example : abcc   
当发现重复字符时c,这个字符重复的可能是刚加入进hash table的c,此时要左移左指针到前一个c才能去掉重复的c
example : abca 
当a为重复字符,左移一位遍可消除重复字符

所以消除字符的过程是一个以hash表不再重负重复为结束条件的while循环

[2/11]leetcode 3090

[3/11]leetcode 1493
删除1个0后有最长的连续1子串,条件转化为窗口里只有一个0的最长子串. 其他逻辑同上

hash table
increase right
count 0
if num of 0>1
left point move forward to decrease the 0. 

[4/11]leetcode 3634
先排序,让窗口变化对逼近边界条件有意义
最大元素小于等于最小元素K倍 Max element <= minimal * K 
