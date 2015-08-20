---
layout: post
title: 回到顶部效果
category: 技术
tags: 技术
description: 慕课网，回到顶部效果@http://www.imooc.com/learn/65
---

### 两种实现方式
- 锚链接实现
`<a href="#"></a>`

优点：简单快速，没有兼容性问题

缺点：视觉上不够直观，用户体验不够好

- JavaScript实现

### 主要知识点
#### DOM操作
- `document.getElementById()` 根据ID获取标签元素
- `document.documentElement.scrollTop` 获取滚动条上沿距离顶部的高度值

#### 事件运用
- `window.onload` 页面加载完毕后触发
- `onclick` 点击后触发
- `window.onscroll` 滚动条滚动时触发

#### 定时器
- `setInterval()` 设置定时器，需传2个参数
- `clearInterval()` 关闭定时器，需传1个参数

### 实现代码
#### 源码链接：<a href="http://codepen.io/zdx/pen/yNdzLj">http://codepen.io/zdx/pen/yNdzLj</a>

#### 代码如下：
HTML
	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
		<html>
		<head>
			<title>backTop</title>
			<link rel="stylesheet" type="text/css" href="style.css" />
			<script type="text/javascript" src="script.js"></script>
		</head>
		<body>
			<div class="box">
				<img src="tb.png" />
			</div>
			<a href="javascript:;" id="btn" title="回到顶部"></a>	<!-- javascript:; ————> 阻止默认返回顶部行为 -->
		</body>
	</html>	