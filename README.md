# vue_practice

[github 地址](https://github.com/wenlong201807/vue_cli_practice)
[码云地址](https://gitee.com/wenlongzhu/vue_practice)

## 脚手架安装步骤

```
0.在github或者码云中复制ssh地址直接在桌面打开git bash(不用建文件夹，克隆的时候会自动生成，生成的文件夹作为跟目录)
1. 全局安装(根目录下)
>npm install --global vue-cli
2. 创建一个基于webpack   模板的新项目
>npm init webpack  my_project(根目录的文件名字)
3. 依据提示，选择必要条件（根目录已经创建，有个提示，选择继续进行）
4. 安装依赖
>npm install
5. 启动
>npm run dev
6. 复制地址，在浏览器中打开
```

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

- 移动端页面 [css reset]("/src/assets/styles/reset.css")

- 移动端 1px 问题\*\*缺失！！

  > import './assets/styles/border.css'
  > css reset->/src/assets/styles/reset.css

- 移动端中，某些机型中有 300 毫秒点击延迟 bug

```
npm install fastclick --save
```

- [阿里云字体图库](http://www.iconfont.cn/manage/index?spm=a313x.7781069.1998910419.11&manage_type=myprojects&projectId=758259)
- 页面跳转写法

<router-link to="/list" class="home">列表页</router-link>
