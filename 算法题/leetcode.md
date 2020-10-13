#### 网址: [leetcode-cn](https://leetcode-cn.com/problemset/all/)

#### 目录: 

* [数组和字符串](#1)
* [链表](#2)
    * [1. 两两交换链表中的结点](https://leetcode-cn.com/problems/swap-nodes-in-pairs/)
* [树与二叉树](#3)
* [队列和栈](#4)
* [堆](#5)
* [二分法](#6)
* [递归与回溯](#7)
* [并查集](#8)
* [位运算](#9)
* [深度优先搜索和广度优先搜索](#10)
* [动态规划](#11)
* [数学题](#12)

***

<h2 id="1"> 1. 数组和字符串 </h2>



<h2 id="2"> 2. 链表 </h2>

[1. 两两交换链表中的结点](https://leetcode-cn.com/problems/swap-nodes-in-pairs/)

假设p、p_next为两个待交换的结点，要保证链表不断，还需要知道p的前驱结点pre、p_next的后继结点p_next_next，思路如下: 

* p为头结点的情况，前驱结点为空，不好处理。因此需要手动给链表添加一个新的头结点newHead。
* p、p_next都不为空才能进行交换

```cpp
class Solution {
public:
    ListNode* swapPairs(ListNode* head) {
        if(!head || !head->next) {
            return head;
        }
        ListNode *newHead = new ListNode(0);
        newHead->next = head;

        ListNode *pre = newHead, *p = head, *p_next = head->next;
        while(p && p_next) {
            ListNode *p_next_next = p_next->next;
            // 结点交换
            pre->next = p_next;
            p_next->next = p;
            p->next = p_next_next;
            // pre和p同步往后移动
            pre = p;
            p = p_next_next;
            p_next = p ? p->next : nullptr;
        }
        return newHead->next;
    }
};
```





<h2 id="3">3. 树与二叉树</h2>



<h2 id="4">4. 队列和栈</h2>



<h2 id="5">5. 堆</h2>



<h2 id="6">6. 二分法</h2>



<h2 id="7">7. 递归与回溯</h2>



<h2 id="8">8. 并查集</h2>



<h2 id="9">9. 位运算</h2>



<h2 id="10">10. 深度优先搜索与广度优先搜索</h2>



<h2 id="11">11. 动态规划</h2>



<h2 id="12">12. 数学题</h2>