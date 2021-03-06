---
title: 数据结构与算法课程 - Chap 3 栈与队列
date: 2019-01-05T01:15:40
description: "数据结构与算法课程期末复习记录 Chapter 3"
featuredImage: "https://alicdn.kmahyyg.xyz/asset_files/aether/cat_school.webp"
categories: ["school"]
draft: false
displayInMenu: false
displayInList: true
dropCap: false
---

# 数据结构复习 - Chapter 3 栈与队列

区分：

L = (a1 ... an)

线性表: 表头、表尾均可插入删除。

栈：只能在表尾进行插入和删除。Last-in-First-Out.

队列：表尾插入，表头删除。 First-in-First-Out.

## 栈

**栈顶指针：总是指向栈顶元素之上的数组下标位置（最上一个可用空间）**
top == base 指针，则栈空。

## 函数调用问题

1. 将当前函数的控制转移到被调用函数的入口
2. 为被调用函数的局部变量分配存储区
3. 将实在参数、返回地址等信息传递给被调用参数保存

### 递归调用

一个直接调用或通过一系列语句间接调用自己的函数成为递归函数。运行规则： **后调用先返回** ，被调用的函数占有的存储管理应当实行 “栈式存储”。

调用顺序： F -> F1 -> F2
返回顺序： F2 -> F1 -> F

## 队列

空队列：队头和队尾指针都指向头节点。
队头指针：永远指向出队的第一个元素位置
队尾：永远指向出队的最后一个元素，判空方法 `Queue.rear == CurrentPtr`

### 循环队列

循环队列：即 设数组维数为 M，使数组下标为 M-1 的结点的指针域，指向数组下标为 0 的结点，从而连成一个环。

若 rear+1 == M, 则令 rear == 0  ( mod 运算)

**注：front 指向队首元素，rear 指向队尾元素的下一个位置**

操作实现:

```
入队：sq[rear]=x    rear=(rear+1) % M
出队：x=sq[front]   front=(front+1) % M
区分队空队满：（用修改后的与不变的做比较）
队空：rear==front        出队操作时才需判断队空
队满：rear==(rear+1)% M  入队时判断队满，即 队头指针在队尾指针的下一个位置 （另外一个解决方案：Q.rear 所指向的单元恒为 NULL）
              ↑
        入队操作修改后的
队列长度： [(Queue.rear - Queue.front + MaxQueueSize) % MaxQueueSize]
```
