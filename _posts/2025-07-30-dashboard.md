---
layout: post
title: "Dashboard架构"
date: 2025-07-30 09:00:00 +0800
categories: 项目
---
## 架构
我的个人博客大多数都写在飞书上，这篇博客有画图和表格，不太好直接复制到github.io中，所以只能以pdf的形式进行展示了

[dashboard架构](/menglan.github.io/寻梦记账看板架构.pdf)

在这篇博客中，详细介绍了dashboard架构初期的思考，但是有的代码随着项目的改进已经有所变化，因为时间有限，无法对博客进行优化了，还请各位面试官见谅

具体代码可以查看[dashboard项目地址](https://github.com/lannastudio/XMDashboard)

## 问题
阅读博客后发现一些问题，虽然有的在项目中暂时还没有修正

1. ComponentFactory初始化数据结构不应该使用+initialize，在我的博客KVO实验一文中提到，+initialize并不总是只被调用一次，KVO就会让+initialize再次调用，所以在这里初始化_factory是不合适的
2. Obsersvable添加观察的类型应该改成NS_OPTIONS，这个问题在项目中已经修正
