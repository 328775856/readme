# 交接文档

标签（空格分隔）： 交接

---

[TOC]

### 一、项目基本说明

大体分为七个项目，在[gitlab](http://192.168.10.189)中项目为 ui 标签中有所体现,最后一个为 app 内嵌页

> - ui-manager
> - ui-customer
> - ui-gbwebsite
> - ui-lease
> - home
> - home-mobile，
> - API MicroService / WebH5MicroService

说明：管理后台项目使用基于 react 的[dva](https://dvajs.com/)和[antd](https://ant.design/index-cn),构建部分使用 webpack 并使用 npm 来管理包，h5 项目使用 h5 标准样式部分使用 less 预处理。

建议：后续可以通过 gitlab 配合 jenkins 服务方式来完成前端的自动部署。

### 二、项目目录说明(已 ui-manager 为例)

     |—config   开发环境下135编辑器配置
     |—public   存放项目静态文件
     |—src
        |—assets    静态文件
        |—common    存放router数据
        |—components    公用组件
        |—layouts       布局组件
        |—models        dva全局model
        |—routes        路由相关组件
        |—services      api请求
        |—utils         工具类js
    |—tests            单元测试
    webpackrc.js    webpack打包相关配置

### 三、前端开发流程

1. 确定项目内容及技术选型，官网、活动及简单页面使用 h5 实现，管理系统使用 dva+antd 框架实现。
2. UI 会将设计图上传至蓝湖，根据蓝湖上设计图还原页面即可。
3. 使用 gitlab 托管项目，不同需求可切不同分支完成再进行合。
4. 发布流程可将项目文件进行打包，将打包后文件压缩为 project-name.zip 交由运维发布。
