---
title: MarkDown学习笔记
author: MIKUMI
top: false
category:
  - Other
tags:
  - MarkDown
abbrlink: da7ed36c
date: 2023-04-08 10:37:38
---
学习makedown的笔记，记录用。
<!--more-->
## 标题
```md
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```
{% note %}
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
{% endnote %}

## 强调
```md
*这个是斜体*  
**这个是粗体**  
***这个是粗斜体***  
~~这个是删除线~~
```
*这个是斜体*  
**这个是粗体**  
***这个是粗斜体***  
~~这个是删除线~~

## 列表
### 无序列表
```md
* 1
  * 1.1  
  * 1.2
* 2
  * 1.2
```
* 1
  * 1.1  
  * 1.2
* 2
  * 1.2

### 有序列表
```md
1. Item 1
2. Item 2  
注意，列表前面的序号其实是无关紧要的，渲染时Markdown会自动修改该序号。
1. Item 3
    1. Item 3a
    2. Item 3b
2. Item 4
    * 有序列表下的无序列表
```
1. Item 1
2. Item 2  
注意，列表前面的序号其实是无关紧要的，渲染时Markdown会自动修改该序号。
1. Item 3
    1. Item 3a
    2. Item 3b
2. Item 4
    * 有序列表下的无序列表

## 表格
```md
| 左对齐 | 右对齐 | 居中对齐 |
| :-| -: | :-: |
| 格 | 格 | 格 |
| 格 | 格 | 格 |
```
| 左对齐 | 右对齐 | 居中对齐 |
| :-| -: | :-: |
| 格 | 格 | 格 |
| 格 | 格 | 格 |

## 链接
```md
[链接名称](https://www.bilibili.com/)  
<https://www.bilibili.com/>
```
[链接名称](https://www.bilibili.com/)  
<https://www.bilibili.com/>

## 图片
```md
![alt 属性文本](图片地址)
![alt 属性文本](图片地址 "可选标题")
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")
```
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")

## 任务列表
```md
* [x] 这个是打勾的任务列表。
* [ ] 这个是没打勾的任务列表。
```
* [x] 这个是打勾的任务列表。
* [ ] 这个是没打勾的任务列表。

## Next主题可用代码
### 按钮
[官方教程链接](https://theme-next.js.org/docs/tag-plugins/button.html)
```
{% button url, text, icon [class], [title] %}
{% btn url, text, icon [class], [title] %}
```
* url：链接地址
* text：按钮上的文本
* icon：Fontswesome图标名称，如果没有指定文本则为必填项。
* \[class\]：可选。Fontswesome图标种类（`fa-fw` `fa-lg` `fa-2x` `fa-3x` `fa-4x` `fa-5x`)
* \[title\]：可选。鼠标悬停在上面的提示。

示例：  
{% button #, 按钮文本, home fa-lg, 悬停显示 %}

### 图片墙
[官方教程链接](https://theme-next.js.org/docs/tag-plugins/group-pictures.html)

### 标签
[官方教程链接](https://theme-next.js.org/docs/tag-plugins/label.html)
```
{% label [class]@text %}
```
* \[class\]：可选。可填以下几个参数
{% label default@default %}
{% label primary@primary %}
{% label success@success %}
{% label info@info %}
{% label warning@warning %}
{% label danger@danger %}
* text：显示的文本。

### 链接组
[官方教程链接](https://theme-next.js.org/docs/tag-plugins/link-grid.html)

### note
[官方教程链接](https://theme-next.js.org/docs/tag-plugins/note.html)
```md
{% note %}
不定义样式
{% endnote %}
```
{% note %}
不定义样式
{% endnote %}

```md
{% note default %}
defaul样式
{% endnote %}
```
{% note default %}
defaul样式
{% endnote %}

```md
{% note primary %}
primary样式
{% endnote %}
```
{% note primary %}
primary样式
{% endnote %}

```md
{% note info %}
info样式
{% endnote %}
```
{% note info %}
info样式
{% endnote %}

```md
{% note success %}
success样式
{% endnote %}
```
{% note success %}
success样式
{% endnote %}

```md
{% note warning %}
warning样式
{% endnote %}
```
{% note warning %}
warning样式
{% endnote %}

```md
{% note danger %}
danger样式
{% endnote %}
```
{% note danger %}
danger样式
{% endnote %}

```md
{% note info no-icon 这里是摘要 %}
折叠测试，info可以换成其他的，no-icon可以去掉。
{% endnote %}
```
{% note info no-icon 这里是摘要 %}
折叠测试，info可以换成其他的，no-icon可以去掉。
{% endnote %}

### 选项卡
[官方教程链接](https://theme-next.js.org/docs/tag-plugins/tabs.html)