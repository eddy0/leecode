# leecode

1. 首先上来先看边界条件, None 和 lengh = 0 的情况


#### 双指针
两个指针解决一个问题
- 普通双指针: 两个指针往同一个方向
- 对撞双指针: 两个指针面对面移动 
    - 一般是有序的
    - 两个指针一个头一个尾
- 快慢双指针: 慢指针 + 快指针
    - 一般是环形链表找重复
    - 指针一个走一步, 一个走两步
    - 需要判断 head 和 head.next 存在

# 对撞双指针套路代码
```py
left = 0
right = len(people) - 1
while (i <= j):
    if 两边之和 < 要求:
        i += 1
    if 两边之和 > 要求:
        j -= 1
    if 两边之和 = 要求:
        处理结果
```

# 快慢指针套路代码
```py
fast = head
slow = head

# 头结点和 next 不为空
if fast is not None or fast.next is not None:
    slow = slow.next
    fast = fast.next.next

```


<!-- GFM-TOC -->

[] 141.环形链表
[] 881.救生艇

* [Leetcode 题解 - 双指针](#leetcode-题解---双指针)
    * [1. 有序数组的 Two Sum](#1-有序数组的-two-sum)
    * [2. 两数平方和](#2-两数平方和)
    * [3. 反转字符串中的元音字符](#3-反转字符串中的元音字符)
    * [4. 回文字符串](#4-回文字符串)
    * [5. 归并两个有序数组](#5-归并两个有序数组)
    * [6. 判断链表是否存在环](#6-判断链表是否存在环)
    * [7. 最长子序列](#7-最长子序列)
<!-- GFM-TOC -->



# 二分查找

重点是要有序
不外乎是 while 循环然后条件变一下
注意区间, 一般写法都是左闭右开的区间, [left, right), 左开右闭, 这样在 while 循环的时候是 right = nums.length, left < right
