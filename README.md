# vue_practice

> A Vue.js project

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

# 我们只需要做的是：

## 下载脚手架之后，启动 npm run dev

-src 中业务代码开发

### 单文件组件与 vue 中的路由

- 单文件组件（.vue）

* 包含三部分，模板 template，scritp，style

- 路由就是根据网址的不同，返回不同的内容给用户
- 405ae7d (HEAD -> master, origin/master, origin/HEAD) 单页面应用配置路由与单页面添加

### 多页面与单页面应用

- 开始。。。
  - 1843436 (HEAD -> master) 开始多页面与单页面
- 多页面应用
- 优点：首屏时间快 ，seo 效果好
- 缺点：页面切换慢
- 页面跳转 只有 HTML 没有 css 没有 js

### 单页面应用

- 优点：页面切换快
- 缺点：首屏时间稍慢，seo 差
- 页面跳转 依靠 js 渲染

### 项目代码的初始化\*\*开始

- 移动端配置第一步

```
屏幕不能放大缩小，手指也不能放大缩小操作
 <meta name="viewport" content="width=device-width,initial-scale=1.0
    minimum-scale=1.0,maximum-scale=1.0,user-scalable=no
    ">
```

- 移动端页面 css reset
  这个是通用的 css reset.这个版本适用于 移动端页面
  如果需要在 PC 端使用，可以 修改 html{font-size: 10px;}为 html{font-size: 12px;}
  其他地方不需要修改

```
=========================================
@charset "utf-8";
html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
font,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td {
    margin: 0;
    padding: 0;
    border: 0;
    outline: 0;
    font-weight: inherit;
    font-style: inherit;
    font-size: 100%;
    font-family: inherit;
    vertical-align: baseline;
}

html {
    font-family: 'sans-serif', "Microsoft YaHei", "微软雅黑", "Tahoma", "Helvetica";
    font-size: 10px;

    background: #fff;
    -webkit-text-size-adjust: 100%;
    -ms-text-size-adjust: 100%;
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0)
}

table {
    border-collapse: collapse;
    border-spacing: 0;
}

img {
    border: 0； max-width: 100%!important;
    vertical-align: middle;
}

address,
caption,
cite,
code,
dfn,
i,
em,
strong,
th,
var {
    font-weight: normal;
    font-style: normal;
}

ol,
ul {
    list-style: none;
}

a {
    text-decoration: none;
}

a:hover,
a:focus {
    outline: none;
}

caption,
th {
    text-align: left;
    font-weight: normal;
}

h1,
h2,
h3,
h4,
h5,
h6 {
    font-weight: normal;
    font-size: 100%;
}

q:before,
q:after {
    content: ”;
}

abbr,
acronym {
    border: 0;
}

button,
input,
optgroup,
select,
textarea {
    margin: 0;
    font: inherit;
    color: inherit;
}

* {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box
}

:before,
:after {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}

input[type=search]::-webkit-search-cancel-button,
input[type=search]::-webkit-search-decoration {
    -webkit-appearance: none;
}

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
nav,
section,
summary {
    display: block;
}

@media screen and (min-width:100px){ /*  iPhone 4,5 */
 html{ font-size: 10px;}
}
@media screen and (min-width:320px){ /*  iPhone 4,5 */
 html{ font-size: 10px;}
}
@media screen and (min-width:375px){ /*  iPhone 6 */
 html{ font-size: 12px;}
}
@media screen and (min-width:414px){  /*  iPhone 6 plus */
 html{ font-size: 12px;}
}
@media screen and (min-width:600px){
    html{ font-size:14px;}
}

红色代码段是为了在不同分辨率手机上，字体缩放
```

- 移动端 1px 问题

  > import './assets/styles/border.css'

- 移动端中，某些机型中有 300 毫秒点击延迟 bug

```
 npm install fastclick --save
```

- [阿里云字体图库](http://www.iconfont.cn/manage/index?spm=a313x.7781069.1998910419.11&manage_type=myprojects&projectId=758259)
- 页面跳转写法

```
<router-link to="/list" class="home">列表页</router-link>
```
