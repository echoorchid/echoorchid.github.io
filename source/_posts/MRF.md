---
title: 马尔科夫随机场解释
date: 2017-02-15 16:21:25
tags: MRF
categories: 基于学习的方法
---
马尔可夫随机场(Markov Random Field)包含两层意思.<!-- more -->
```
A.马尔可夫性质：
它指的是一个随机变量序列按时间先后关系依次排开的时候，
第N+1时刻的分布特性，与N时刻以前的随机变量的取值无关。
 
比方：
拿天气来打个比方。
如果我们假定天气是马尔可夫的，其意思就是我们假设
今天的天气仅仅与昨天的天气存在概率上的关联，
而与前天及前天以前的天气没有关系。
其它如传染病和谣言的传播规律，就是马尔可夫的。 
 
B.随机场：
当给每一个位置中按照某种分布随机赋予相空间的一个值之后，
其全体就叫做随机场。
 
比方：
我们不妨拿种地来打个比方。
其中有两个概念：位置（site），相空间（phase space）。
“位置”好比是一亩亩农田；
“相空间”好比是种的各种庄稼。
我们可以给不同的地种上不同的庄稼，
这就好比给随机场的每个“位置”，赋予相空间里不同的值。
所以，俗气点说，随机场就是在哪块地里种什么庄稼的事情。 
 
马尔可夫随机场：
拿种地打比方，如果任何一块地里种的庄稼的种类
仅仅与它邻近的地里种的庄稼的种类有关，
与其它地方的庄稼的种类无关，那么这些地里种的庄稼的集合，
就是一个马尔可夫随机场。
```