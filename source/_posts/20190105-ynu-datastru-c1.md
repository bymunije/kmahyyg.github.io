---
title: 数据结构与算法课程 - Chap 1 序言
date: 2019-01-05 01:14:49
tags:
  - School
  - Datastru
---

# 数据结构复习 - Chapter 1 序言

## 导论

数据结构研究： 数据的 **逻辑结构、存储结构、每种结构定义的运算** 。

相关概念：
- 数据：信息的符号表示
- 数据元素：数据的基本单位
- 数据项：一个数据元素可由若干个数据项组成，**数据项是数据的不可分割的最小单位**。
- 数据对象：性质相同的数据元素的集合，数据的一个子集。
- 结构：数据彼此之间存在的相互关系。
- 数据结构：相互之间存在的一种或多种特定关系的数据元素的集合。元素之间的相互联系称为逻辑结构。

逻辑结构包括：
- 集合：没有相关性。
- 线性关系：一对一。
- 树形关系：一对多。
- 图状结构：多对多。

## ADT 抽象数据类型描述
表示对应数学模型及定义在该模型上的一组操作。

```
ADT Typename{
  Object: Definition
  Relationship: Definition
  BasicOperation: Definition
} ADT Typename
```

## 算法
算法：指令的有限序列，每条指令包括一个或多个操作，五个特性：**有穷、确定、可行性、输入、输出** 。

算法意味着 **可终止** ，程序是 **算法使用某种具体程序设计语言** 具体实现。

算法的设计要求：
- 正确性： 满足具体问题需求。
- 可读性：有助于阅读理解，简化后续维护与调试修改的难度。
- 健壮性（Robustness，鲁棒性）：具有容错处理能力。
- 效率 与 存储需求：算法执行时间 + 算法执行过程中所需的最大存储空间，与问题规模相关。

### 算法构成与复杂度问题

时间复杂度 <=> 运算工作量，对应问题规模
空间复杂度 <=> 对应需要的最大存储空间

算法：控制结构（循环、顺序、分支）+原操作（固有数据类型的操作）

例如：三次循环，从1到n，总次数为 n^3 ，时间复杂度为 O(n^3)
 
