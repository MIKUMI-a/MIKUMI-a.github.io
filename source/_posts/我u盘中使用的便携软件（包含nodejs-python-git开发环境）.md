---
title: 我U盘中使用的便携软件的简要介绍
date: 2024-03-06 10:28:40
author: MIKUMI
top: false
sidebar: true
toc: true
tags:
  - U盘，便携软件
categories:
  - U盘
comments: false
description: 包含NodeJs/Python/Git开发环境，还有便携软件网站的分享。
---
便携软件网站（以下的软件我没给地址的都可以在这些网站中找到，部分需要科学上网）：

- [PortableApp](https://portableappk.com/)
- [PortableAppZ](http://portableappz.blogspot.com/)
- [荷花绿色便携软件](https://www.hehuasoft.com/)
- [jooseng6的微博](https://weibo.com/2787439924)
- [PortableAppK（部分需要付费才能下）](https://portableappk.com/)

## ## 7-Zip

不必多说，虽然大部分电脑应该都会有解压软件，但我爹就不喜欢装，反正不大就留着了。

## Audacious

听歌软件，不过我很少听，追求能响就行，它支持相对路径，挺好用的。

## 百度网盘

我也不想留，但是实在是用它的地方太多了。

## 百分浏览器

用过很多支持便携的浏览器，它是最流畅的，而且支持谷歌插件，满足我的使用需求了。[在这里下载便携版](https://www.centbrowser.cn/history.html)

## Clash for Windows

停止更新了，但是我离不开它，一直在用旧版的。

> 变成便携版的方式：在同级目录内新建data文件夹。

## CLaunch

自带便携版，支持相对路径，功能很多，虽然我更习惯用UTools，但UTools完全不能便携，这个还是挺好用的。[下载地址（下Zip文件）](https://hp.vector.co.jp/authors/VA018351/en/claunch.html)

## DiskGenius

磁盘管理软件，我也不知道它便不便携，但是就是得用它，功能全面，装机必备。[官网](https://www.diskgenius.cn/)

## Dism++

超好用的系统优化工具，装机必备。[下载地址](https://github.com/Chuyu-Team/Dism-Multi-language/releases)

## 天翼云盘

留着备用，毕竟百度网盘真的太慢了。

## eDiary

笔记软件，同步功能比不上Joplin，界面也有点儿古早，但是体积小巧，如果没有太大需求可以用它。[下载地址](http://www.haoxg.net/ediary/download_windows.html)

## Everything

这就是神，不必多解释。除了界面真的很朴素之外，没有缺点。

## HotSwap!

用来热插拔U盘，因为U盘内开的软件多了就很难弹出U盘了，在写了个bat文件CLaunch关闭时运行就可以顺便弹出U盘了。[官网](http://mt-naka.com/hotswap/index_enu.htm#download)

> bat文件内的代码：`HotSwap! %~d0`

## IrfanView

图片查看工具，总有用得上的时候。

## Joplin

笔记工具，官方自带便携版（下载地址在文档里有点儿隐蔽）在文档里，才刚刚用，同步功能超好用，虽然我更喜欢notion的那种看板，但是这个感觉其实也不错。（反正看板我做完也是吃灰的）[便携版下载地址](https://joplinapp.org/help/install)

## Notepad2

代替系统自带的记事本，小巧好用，打开超快速。

[下载地址](https://www.flos-freeware.ch/notepad2.html)

在PE中更改默认记事本的bat文件代码（放在在EXE文件同级目录）：

```
reg add "HKLM\Software\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\notepad.exe" /v "Debugger" /t REG_SZ /d "\"%~dp0Notepad2.exe\" /z" /f

```

## 万彩工具箱

办公必备，功能很多，包含PDF格式转换等功能。

## Photoshop CC

我真的离不开PS，改图片大小都想用它，但是我忘记这个便携版是从哪儿下的了。

## PicGo

好用的图床工具，写博客必备（虽然我真的不怎么写）。

## PortableApps

便携软件管理工具，从[PortableApps.com](PortableApps.com)下的软件都可以通过这个软件更新，虽然我只有在想更新的时候打开它。

## PotDesktop

划词翻译，刚下的，不咋会用。

## PotPlayer

超棒的视频软件（但是我不常用，基本都在看B站）

## QQ

功能强大，它也很大，但是我离不开它，还是留着吧。

## Snipaste

截图软件，还可以贴图，但是我最常用的是QQ。（所以明白我为什么离不开QQ了吧）[官网](https://zh.snipaste.com/)

## 迅雷

虽然……但要用的时候还是得用它。

## Scrcpy

手机投屏工具，我用的GUI是B站UP 晨钟酱Official 的。[B站地址](https://www.bilibili.com/video/BV1pU4y1b7kE/)

## VSCode

功能强大，我一直以为它很大，但是打开超快速。写代码、搭建博客、管理git都很好用。[下载地址](https://code.visualstudio.com/download)

> 变成便携版的方式：下载zip包，解压后在同级目录内新建data文件夹。

## 关于微信

因为“小而美”实在有些大，而且我不常用，所以现在在用网页版的。

[微信网页版地址](https://wx.qq.com/)

但使用它需要在浏览器里装这个插件[Github地址](https://github.com/lqzhgood/wechat-need-web)

## 开发环境

我的U盘里还是得放nodejs、git和python的，有时会用到（无聊摸鱼）。

我全都放在同一个文件夹了，方便写bat文件。

### NodeJs

[下载地址](https://nodejs.cn/download/)在这下Zip包解压。这还没完，不然他还是会把模块缓存等放在系统文件夹里的。请看我之后的Bat文件写法。

### Git

[下载地址](https://git-scm.com/download/win)下便携版。虽然是便携版但是配置文件依然放在系统用户文件夹，所以还是得看后面的bat文件。

### Python

这个比较麻烦，而且我需要的是完全版的Python，不能使用嵌入版的，WinPython也很好用，但是我在我的PE里用不了。下面我也是参考了别人的做法。

[下载地址](https://www.python.org/downloads/windows/)

- 需要先下`Windows installer`版本安装在电脑上。
- 一般的安装地址是`C:\Users\[你的用户名]\AppData\Local\Programs\Python`，到这里把Python文件程序文件夹复制到U盘。
- 接下来有点儿麻烦，打开Python文件程序文件夹中的Scripts文件夹。
- 用Notepad2等软件修改其中的exe文件（所有文件都需要修改，如果有新增的也需要修改）。划到最底部，修改红线位置。

![改前](https://s2.loli.net/2024/03/05/mEYaOIx8wySVsnl.png)

![改后](https://s2.loli.net/2024/03/05/4mFsRHLrSuWl5IX.png)

### 最终设置

目前文件夹是这样的：

![文件夹](https://s2.loli.net/2024/03/05/JCzLRsmGKZ18b62.png)

像我这样新建个`evi.bat`文件，代码如下：

```

@echo off

set "USERPROFILE=%~d0\Documents"
set "PYTHON_PATH=%~dp0python"
set "NODE_PATH=%~dp0node"
set "GIT_PATH=%~dp0PortableGit"

set "PATH=%PYTHON_PATH%;%PYTHON_PATH%\Scripts;%PYTHON_PATH%\DLLs;%NODE_PATH%;%NODE_PATH%\node_global;%GIT_PATH%\bin;%PATH%"

call npm config set prefix "%NODE_PATH%\node_global"
call npm config set cache  "%NODE_PATH%\node_cache"
call npm config set registry https://registry.npm.taobao.org

cd %USERPROFILE%
%1

```

`%~d0\Documents`位于U盘根目录的Documents文件夹，使用PortableApps的话它会自己创建的，我在这把它用作用户文件夹，一些设置文件会放在这里。不喜欢的话可以自行修改。

使用时可以把程序拖入，也可以把末尾的`%1`改成你想启动的程序，比如改成`CMD.exe`打开它就可以使用带有便携环境的命令行了。

也可以这么使用，例如我的VSCode所用的Bat（前提是不要改变最后的`%1`)：

```
@echo off
set "APPS=%~d0\PortableApps"
%APPS%\CommonFiles\evi.bat "%APPS%\VSCode\Code.exe"
```

## 尾言

便携软件自己研究了挺久的，经验大部分都是从网上学的，如果有变化也会更新的。原来是兼容Win7的，但是有太多软件新版都不支持Win7了（比如python、VSCode等)，如果需要兼容的话请使用低版本的。
