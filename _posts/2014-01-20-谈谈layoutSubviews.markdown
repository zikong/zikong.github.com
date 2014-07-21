---
title: 谈谈layoutSubviews
layout: post
guid: urn:uuid:2557955c-e71c-4a3a-9d0a-be9a9bb6737c
tags:
  - UIView
  - IOS
---

今天我们来谈一谈UIView里的一个方法：*layoutSubviews*；
```
	- (void)layoutSubviews
```
当你重写该方法时，可以约束子视图的布局。子视图无法改变这个布局，除非重写该方法。但是你又不能
直接调用该方法，如果你想强制更新布局你可以调用*layoutIfNeeded*方法。

但是如果你需要在外部设置子视图的布局就不要重写该方法，如果你实在想用那也可以参考*UIButton*
的实现方式，设置*UIEdgeInsets*属性。通过设置*UIEdgeInsets*属性来改变子视图的布局。
