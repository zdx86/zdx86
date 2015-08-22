---
layout: post
title: CSS进行网页布局
category: 技术
tags: css layout
description: 慕课网，CSS进行网页布局@http://www.imooc.com/learn/57
---
来源：<a href="http://www.imooc.com/learn/57">http://www.imooc.com/learn/57</a>

### 布局
又称版式布局，是网页Ui设计师将有限的视觉元素进行有机的排列组合。
网页设计的特点：
- 网页可以自适应宽度
- 网页的长度理论没有限制

分栏。又称为`分列`，常见布局有一列、二列、三列等以及混合布局。

### 一列布局
往往作为网站的首页，不适合放置多行文本。一般都是固定宽度。
#### 一列固定
	<!DOCTYPE html>
	<html>
		<head>
		<title>一列布局</title>
		<style>
			body{ margin:0; padding:0;/*清除默认样式*/}
			div{ text-align:center; font-weight:bold}
			.head, .main, .footer{ width:960px; margin:0 auto}
			.head{ height:100px; background:#ccc}
			.main{ height:600px; background:#FCC}
			.footer{ height:50px; background:#9CF}
		</style>
	
		</head>
		<body>
			<div class="head">head</div>
			<div class="main">main</div>
			<div class="footer">footer</div>
		</body>
	</html>

#### 一列自适应
	.head, .main, .footer{width:80%;margin:0 auto}

### 二列布局
#### 二列自适应

	<div class="left">left</div>
	<div class="right">right</div>

样式如下：

	.left{ width:20%; height:600px; background:#ccc; float:left}
	.right{ width:80%; height:600px; background:#FCC; float:right}

#### 二列居中自适应
	<div class="main">
	    <div class="left">left</div>
	    <div class="right">right</div>
	</div>

样式如下：

	.main{ width:80%; height:600px; margin:0 auto}
	.left{ width:20%; height:600px; background:#ccc; float:left}
	.right{ width:80%; height:600px; background:#FCC; float:right}

#### 二列居中固定

	.main{ width:960px; height:600px; margin:0 auto}
	.left{ width:300px; height:600px; background:#ccc; float:left}
	.right{ width:660px; height:600px; background:#FCC; float:right}
### 三列布局
注意此时需用`position`，使用`float`达不到效果
#### 三列自适应
	<div class="left">left</div>
    <div class="main">main</div>
    <div class="right">right</div>
样式如下：
	.left{ width:20%; height:600px; background:#ccc; position:absolute; left:0; top:0}
	.main{ height:600px; margin:0 20%; background:#9CF}
	.right{ height:600px; width:20%; position:absolute; top:0; right:0; background:#FCC;}

#### 三列左右固定

	.left{ width:240px; height:600px; background:#ccc; position:absolute; left:0; top:0}
	.main{ height:600px; margin:0 240px; background:#9CF}
	.right{ width:240px;height:600px;  position:absolute; top:0; right:0; background:#FCC;}

### 混合布局

#### 混合1
	<div class="head">head</div>
	<div class="left">left</div>
	<div class="right">right</div>

样式如下：

	<div class="head">head</div>
	<div class="left">left</div>
	<div class="right">right</div>

#### 混合2
	<div class="head">head</div>
	<div class="main">
	    <div class="left">left</div>
	    <div class="right">right</div>
	</div>
	<div class="footer">footer</div>

样式如下：

	.head, .main, .footer{ width:960px; margin:0 auto}
	.head{ height:100px;background:#9CF}
	.left{ width:240px; height:600px; background:#ccc; float:left}
	.right{ width:720px; height:600px;background:#FCC; float:right}
	.footer{ height:50px; background:#9F9; clear:both}

#### 混合3
	.head, .main, .footer{ width:960px; margin:0 auto}
	.head{ height:100px;background:#9CF}
	.left{ width:240px; height:600px; background:#ccc; float:left}
	.right{ width:720px; height:600px;background:#FCC; float:right}
	.footer{ height:50px; background:#9F9; clear:both}

样式如下：

	.head, .main, .footer{ width:960px; margin:0 auto}
	.head{ height:100px;background:#9CF}
	.left{ width:220px; height:600px; background:#ccc; float:left}
	.right{ width:740px; height:600px;background:#FCC; float:right}
	.r_sub_left{ width:540px; height:600px; background:#9C3; float:left}
	.r_sub_right{ width:200px; height:600px; background:#9FC; float:right}
	.footer{ height:50px; background:#9F9; clear:both}

#### 混合4
	.head, .main, .footer{ width:960px; margin:0 auto}
	.head{ height:100px;background:#9CF}
	.left{ width:220px; height:600px; background:#ccc; float:left}
	.right{ width:740px; height:600px;background:#FCC; float:right}
	.r_sub_left{ width:540px; height:600px; background:#9C3; float:left}
	.r_sub_right{ width:200px; height:600px; background:#9FC; float:right}
	.footer{ height:50px; background:#9F9; clear:both}

样式如下：

	.head, .main, .footer{ width:960px; margin:0 auto}
	.head{ height:100px;background:#9CF}
	.left{ width:220px; height:600px; background:#ccc; float:left}
	.right{ width:740px; height:600px;background:#FCC; float:right}
	.r_sub_left{ width:540px; height:600px; background:#9C3; float:left}
	.r_sub_right{ width:200px; height:600px; background:#9FC; float:right}
	.footer{ height:50px; background:#9F9; clear:both}