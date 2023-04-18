---
title: blog美化记录
author: MIKUMI
top: false
sidebar: true
toc: true
category:
  - Other
tags:
  - Hexo
  - Next
abbrlink: 9b1c2aff
date: 2023-04-08 14:15:08
---
目前这个blog所美化的代码及总结。
<!--more-->
> **使用软件及其版本：**  
> node: 12.22.12  
> hexo: 5.4.2  
> hexo-cli: 4.3.0  
> git: 2.40.0.windows.1  
> hexo-theme-next

## 侧边栏添加播放器，且切换网页不会中断
1. 安装[hexo-tag-aplayer](https://github.com/MoePlayer/hexo-tag-aplayer)
   ```node
   npm install --save hexo-tag-aplayer
   ```
2. 在`_config.yml`中添加设置
   ```
   aplayer:
     meting: true
     asset_inject: false
   ```
3. 在博客目录下的`source/_data/header.njk`（没有文件夹或文件就新建）写入以下代码。
   ```html
   <!-- 引用Aplayer和metingjs-->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/aplayer@1.10.1/dist/APlayer.min.css">
    <script src="https://cdn.jsdelivr.net/npm/aplayer@1.10.1/dist/APlayer.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/meting@1.2.0/dist/Meting.min.js"></script>
    <div id="my-aplayer"
    class="aplayer"
    data-id="8276622146" // 必须，歌曲id、播放列表id、相册id、搜索关键字
    data-server="netease" // 必须，音乐平台: netease, tencent, kugou, xiami, baidu
    data-type="playlist" // 必须，song, playlist, album, search, artist
    data-fixed="false" // 吸底模式可以固定播放器于页面底部，但是这里我要放在侧边栏中，所以是false
    data-fixed="true" // 开启固定模式
    data-autoplay="false" // 自动播放
    data-order="random" // 列表播放模式:list,random
    data-volume="0.8" 
    data-theme="#be98aa"
    data-preload="auto"
    data-mutex="true"
    data-listfolded="true"
    ></div>
   ```
4. 修改`_config.next.yml`文件
   * `custom_file_path`下的`header: source/_data/header.njk`取消注释。
   * 修改`pjax`项为true，如`pjax: true`。

## Next主题颜色样式美化
1. 博客目录下新建`source/_data/header.njk`。
2. 修改`_config.next.yml`文件，`custom_file_path`下的`style: source/_data/styles.styl`和`variable: source/_data/variables.styl`取消注释。
   * `styles.styl`文件是用来修改样式的。
   * `variables.styl`文件是用来修改颜色变量的。

### variables.styl
仅放出我的代码，因为具体的我也不太清楚。
```styl
$whitesmoke   = hsl(22, 40%, 96%);
$gainsboro    = hsl(22, 38%, 93%);
$grey-lighter = hsl(22, 36%, 87%);
$grey-light   = hsl(22, 34%, 80%);
$grey         = hsl(22, 32%, 73%);
$grey-dark    = hsl(23, 30%, 60%);
$grey-dim     = hsl(23, 28%, 40%);
$black-light  = hsl(23, 26%, 33%);
$black-dim    = hsl(23, 24%, 20%);
$black-deep   = hsl(23, 22%, 13%);
$red          = #bf477f;
$blue-bright  = #fcd7e8;
$blue         = #dca0b2;
$blue-deep    = #be98aa;
$orange       = #465e65;
```

### styles.styl
#### 设置背景
```styl
body {
    /* 设置背景颜色 */
    margin: 0;
    background-color: #be98aa;
    background-image: 
    radial-gradient(closest-side, rgba(170, 142, 245, 1), rgba(235, 105, 78, 0)),
    radial-gradient(closest-side, rgba(190, 151, 170, 1), rgba(243, 11, 164, 0)),
    radial-gradient(closest-side, rgba(254, 234, 131, 1), rgba(254, 234, 131, 0)),
    radial-gradient(closest-side, rgba(190, 151, 170, 1), rgba(170, 142, 245, 0)),
    radial-gradient(closest-side, rgba(248, 192, 147, 1), rgba(248, 192, 147, 0));
    background-size: 
    130vmax 130vmax,
    80vmax 80vmax,
    90vmax 90vmax,
    110vmax 110vmax,
    90vmax 90vmax;
    background-position:
    -80vmax -80vmax,
    60vmax -30vmax,
    10vmax 10vmax,
    -30vmax -10vmax,
    50vmax 50vmax;
    background-repeat: no-repeat;
}
```

#### 设置各部分背景透明度
```styl
//文章内容透明度设置
.content.wrap {
    opacity: 0.6;
    }
.post-block {
    background: rgba(255,255,255,0.5) none repeat scroll !important;
    }
//菜单透明
.header{
    background: rgba(255,255,255,0.5) none repeat scroll !important;
    }
//边栏透明
.sidebar-inner{
    background: rgba(255,255,255,0.5) none repeat scroll !important;
    }
//评论区透明（不知道有没有用）
.comments{
    background: rgba(255,255,255,0.5) none repeat scroll !important;
    }
```
#### 文章标题样式
```styl
h1
    color #3e3f4c
h2
    margin .5em auto
    color #3e3f4c
    padding-bottom 5px
    font-size 1.5rem
    &::before
        color #be98aa
        content "\f70e  "
        width: 9px
        height: 9px
        font-family: FontAwesome
h3
    margin .5em auto
    color #be98aa
    background #3e3f4c
    border-left 4px solid #be98aa
    padding .2em .6em
    box-shadow 1px 1px 1px rgba(0,0,0, .1)
    &:hover a
        text-decoration underline
    &::after
        content " \f061"
        width: 9px
        height: 9px
        font-family: FontAwesome
h4, h5, h6
    margin-top 20px
    padding-bottom 5px
    border-bottom 1px solid #ddd
h4::before
    color #be98aa
    content "\f4d8  "
    width: 9px
    height: 9px
    font-family: FontAwesome
h5::before
    color #be98aa
    content "\f0c2  "
    width: 9px
    height: 9px
    font-family: FontAwesome
h6::before
    color #be98aa
    content "\f004  "
    width: 9px
    height: 9px
    font-family: FontAwesome
```
#### blockquote
```styl
blockquote
    padding .4em 20px
    margin .5em auto
    border-left 4px solid #af888a
    background rgba(241, 229, 222,1)
    box-shadow 1px 1px 1px rgba(0,0,0, .1)
    p
        margin .4em auto
    blockquote
        border-left none
    footer
        font-style italic
        cite::before
            content "—"
            padding 0 .3em
```

#### 按钮设定(就改了一下颜色)
```styl
//按钮 .btn
.btn
  background rgba(255, 255,255,0)
  border 2px solid #3e3f4c
  color #3e3f4c
  &:hover
    background #3e3f4c
    border-color #be98aa
    color #be98aa
```

#### 其他的一些颜色设置
```styl
//页脚字体颜色
.footer{
    color: #000
    }
//右上角的标题字体颜色
.site-title{
    color: #be98aa
    }
.site-subtitle{
    color: #be98aa
    }
```