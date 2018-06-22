
## Introduction(简介)

**AdminLTE with iframe** -- Based on **AdminLTE** framework. It integrated with iframes with is popular in china admin systems.

(基于AdminLTE框架,并且集成了iframe的tab页面,是一款适合中国国情的后台主题UI框架)

**Preview on github: [https://weituotian.github.io/AdminLTE-With-Iframe/pages/index_iframe.html](https://weituotian.github.io/AdminLTE-With-Iframe/pages/index_iframe.html)**

**Preview on oschina: [http://weituotian.oschina.io/adminlte-with-iframe/pages/index_iframe.html](http://weituotian.oschina.io/adminlte-with-iframe/pages/index_iframe.html)**


![preview image1](preview/GIF.gif)

![preview image2](preview/img1.png)

## Table of Contents(目录)
<!-- MarkdownTOC -->

- [1. branch\(分支\)](#1-branch%E5%88%86%E6%94%AF)
- [2. reference\(参考\)](#2-reference%E5%8F%82%E8%80%83)
- [3. Installation\(安装\)](#3-installation%E5%AE%89%E8%A3%85)
- [4. 目录结构](#4-%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84)
- [5. Documentation\(文档\)](#5-documentation%E6%96%87%E6%A1%A3)
    - [5-1. 整合到您的项目](#5-1-%E6%95%B4%E5%90%88%E5%88%B0%E6%82%A8%E7%9A%84%E9%A1%B9%E7%9B%AE)
    - [5-2. iframe框架](#5-2-iframe%E6%A1%86%E6%9E%B6)
        - [5-2-1. 选项卡右键菜单，双击刷新](#5-2-1-%E9%80%89%E9%A1%B9%E5%8D%A1%E5%8F%B3%E9%94%AE%E8%8F%9C%E5%8D%95%EF%BC%8C%E5%8F%8C%E5%87%BB%E5%88%B7%E6%96%B0)
        - [5-2-2. 一些配置](#5-2-2-%E4%B8%80%E4%BA%9B%E9%85%8D%E7%BD%AE)
        - [5-2-3. 左侧菜单生成](#5-2-3-%E5%B7%A6%E4%BE%A7%E8%8F%9C%E5%8D%95%E7%94%9F%E6%88%90)
        - [5-2-4. tab的操作](#5-2-4-tab%E7%9A%84%E6%93%8D%E4%BD%9C)
            - [5-2-4-1. 增加新tab](#5-2-4-1-%E5%A2%9E%E5%8A%A0%E6%96%B0tab)
            - [5-2-4-2. 获得当前激活的tab的id](#5-2-4-2-%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8D%E6%BF%80%E6%B4%BB%E7%9A%84tab%E7%9A%84id)
            - [5-2-4-3. 获得当前激活的tab的id](#5-2-4-3-%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8D%E6%BF%80%E6%B4%BB%E7%9A%84tab%E7%9A%84id)
            - [5-2-4-4. 根据pageId获得当前选项卡的标题](#5-2-4-4-%E6%A0%B9%E6%8D%AEpageid%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8D%E9%80%89%E9%A1%B9%E5%8D%A1%E7%9A%84%E6%A0%87%E9%A2%98)
            - [5-2-4-5. 根据pageId获得当前iframe](#5-2-4-5-%E6%A0%B9%E6%8D%AEpageid%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8Diframe)
            - [5-2-4-6. 根据pageId获得当前panel](#5-2-4-6-%E6%A0%B9%E6%8D%AEpageid%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8Dpanel)
            - [5-2-4-7. 关闭tab](#5-2-4-7-%E5%85%B3%E9%97%ADtab)
            - [5-2-4-8. 刷新tab](#5-2-4-8-%E5%88%B7%E6%96%B0tab)
            - [5-2-4-9. 未完待续](#5-2-4-9-%E6%9C%AA%E5%AE%8C%E5%BE%85%E7%BB%AD)
- [6. Browser Support\(浏览器支持\)](#6-browser-support%E6%B5%8F%E8%A7%88%E5%99%A8%E6%94%AF%E6%8C%81)
- [7. License](#7-license)
- [8. Todo List](#8-todo-list)
- [9. 相关示例项目](#9-%E7%9B%B8%E5%85%B3%E7%A4%BA%E4%BE%8B%E9%A1%B9%E7%9B%AE)

<!-- /MarkdownTOC -->

<a id="1-branch%E5%88%86%E6%94%AF"></a>
## 1. branch(分支)

更新分支为master

<a id="2-reference%E5%8F%82%E8%80%83"></a>
## 2. reference(参考)

**[super ui](https://github.com/tzhsweet/superui)**

(iframe功能的js和页面css都是参考superui得出来的)

<a id="3-installation%E5%AE%89%E8%A3%85"></a>
## 3. Installation(安装)

修改可以使用grunt构建工具

- 安装nodejs
- 项目根目录下命令行执行
- npm install grunt-cli -g
- npm install

<a id="4-%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84"></a>
## 4. 目录结构
- build/js/iframe 存放所有关于iframe的源代码，强烈建议修改这里的代码
- dist/js/app_iframe.js 使用grunt构建工具生成的js，属于打包后的js

<a id="5-documentation%E6%96%87%E6%A1%A3"></a>
## 5. Documentation(文档)

may be you should **customize** the system by reading the codes!
(请阅读源码进行修改)  

[AdminLTE官方文档](http://weituotian.oschina.io/adminlte-with-iframe/documentation/index.html)


<a id="5-1-%E6%95%B4%E5%90%88%E5%88%B0%E6%82%A8%E7%9A%84%E9%A1%B9%E7%9B%AE"></a>
### 5-1. 整合到您的项目
1. 负责 `plugins`, `dist` 目录到您的项目中
1. 复制 [index_iframe.html](pages/index_iframe.html) 到您的项目中，
    1. 修改引用的js路径，css路径，比如Java Web要用到${ContextPath}之类的。
    1. 也可修改其中的创建菜单的js
1. 子iframe的页面可以复制模板 [welcome_iframe.html](pages/welcome_iframe.html)

<a id="5-2-iframe%E6%A1%86%E6%9E%B6"></a>
### 5-2. iframe框架

介绍一些集成了iframe后新增的功能，和修改方法。
请确认执行完上面文档的安装部分。
可随时开启issue.

<a id="5-2-1-%E9%80%89%E9%A1%B9%E5%8D%A1%E5%8F%B3%E9%94%AE%E8%8F%9C%E5%8D%95%EF%BC%8C%E5%8F%8C%E5%87%BB%E5%88%B7%E6%96%B0"></a>
#### 5-2-1. 选项卡右键菜单，双击刷新

![](preview/contextmenu.jpg)

* 修改右键菜单的文字，请参阅 [bootstrap-tab.js](build/js/iframe/bootstrap-tab.js) ，内有`context.attach`初始化json菜单，并且可以参考其获取特定tab当前url的代码
* 刷新选项卡刷新当前tab页，bootstrap-tab.js中的`$tabs.on("dblclick",`绑定了双击事件。可注释取消这个功能

<a id="5-2-2-%E4%B8%80%E4%BA%9B%E9%85%8D%E7%BD%AE"></a>
#### 5-2-2. 一些配置

在 [index_iframe.html](pages/index_iframe.html) 中：

```
//设置根目录，
//比如本演示中的地址是http://weituotian.oschina.io/adminlte-with-iframe/pages/index_iframe.html#
//上一级就是http://weituotian.oschina.io/adminlte-with-iframe/pages
//当前实际的开发中一般用不到
//比如你的首页用到index_iframe.html这个模版，访问地址为http://localhost/，就不用设置了
//如果你部署在http://localhost/xxx, xxx是你部署的路径，那么就按以下代码设置一下根目录
App.setbasePath("../");

//设置图片路径，相对于根目录
//这个框架带有一些图片（加载进度条等），你可以放置在其它地方
//但要如下设置，
//比如在本项目中，引用的图片放在了根目录下，dist/img/中
App.setGlobalImgPath("dist/img/");

```

<a id="5-2-3-%E5%B7%A6%E4%BE%A7%E8%8F%9C%E5%8D%95%E7%94%9F%E6%88%90"></a>
#### 5-2-3. 左侧菜单生成

如下操作，可参考 index_iframe.html, [sidebarMenu.js](build/js/iframe/sidebarMenu.js)
```
        var menus = [
            {
                id: "9000",
                text: "header",
                icon: "",
                isHeader: true
            },
            {
                id: "9002",
                text: "Forms",
                icon: "fa fa-edit",
                children: [
                    {
                        id: "90021",
                        text: "advanced",
                        url: "forms/advanced_iframe.html",
                        targetType: "iframe-tab",
                        icon: "fa fa-circle-o"
                    },
                    {
                        id: "90022",
                        text: "general",
                        url: "forms/general_iframe.html",
                        targetType: "iframe-tab",
                        icon: "fa fa-circle-o"
                    },
                    {
                        id: "90024",
                        text: "百度",
                        url: "https://www.baidu.com",
                        targetType: "iframe-tab",
                        icon: "fa fa-circle-o",
                        urlType: 'abosulte'
                    }
                ]
            }
        ];
        $('.sidebar-menu').sidebarMenu({data: menus});
```


<a id="5-2-4-tab%E7%9A%84%E6%93%8D%E4%BD%9C"></a>
#### 5-2-4. tab的操作

所有的操作都可以在index_iframe.html中实现。index_iframe.html作为一个父页面承载了许多iframe。以下介绍的函数可以主页面使用, 在iframe子页面，也可以通过`top.xxx`来调用父页面的函数。
以下函数可以打开chrome控制台进行测试操作。

<a id="5-2-4-1-%E5%A2%9E%E5%8A%A0%E6%96%B0tab"></a>
##### 5-2-4-1. 增加新tab
动态增加菜单，你可以从后台读取菜单，用以下的json格式封装。同时还可以自己额外增加菜单
```
//欢迎页的菜单。
        addTabs({
            id: '10008',
            title: '欢迎页',
            close: false,
            url: 'welcome_iframe.html',
            urlType: "relative"
        });
```

- **id** 代表这个tab的id，重复id将认为同一个tab，如果你从数据库读取菜单，那么可以设置该id为数据库中菜单的id
- **title** 选项卡的标题
- **close**　false表示不可以关闭
- **url** 指定一个url地址，绝对或者相对地址
- **urlType** 可选relative和absolute ,默认是relative, 相对于当前页面（管理所有tab的页面）
比如`http://localhost/index.html`,想打开index.html同级目录UI下的页面，就给`url:UI/welcome.html;urlType:relative`

<a id="5-2-4-2-%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8D%E6%BF%80%E6%B4%BB%E7%9A%84tab%E7%9A%84id"></a>
##### 5-2-4-2. 获得当前激活的tab的id
```
var pageId = getActivePageId();
```
最常用吧，一般这个就够了, 在子iframe页面用`top.getActivePageId()`获取,以下的函数类同。
有了pageId，我们可以调用其它函数操作page。

<a id="5-2-4-3-%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8D%E6%BF%80%E6%B4%BB%E7%9A%84tab%E7%9A%84id"></a>
##### 5-2-4-3. 获得当前激活的tab的id

```
var pageId = getPageId(element);
```

![](preview/tabs.jpg)
element一般是tab栏的a超链接元素，jq对象和普通的dom都可以

<a id="5-2-4-4-%E6%A0%B9%E6%8D%AEpageid%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8D%E9%80%89%E9%A1%B9%E5%8D%A1%E7%9A%84%E6%A0%87%E9%A2%98"></a>
##### 5-2-4-4. 根据pageId获得当前选项卡的标题
```
var title = findTabTitle(pageId);
```


<a id="5-2-4-5-%E6%A0%B9%E6%8D%AEpageid%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8Diframe"></a>
##### 5-2-4-5. 根据pageId获得当前iframe

```
var $iframe = findIframeById(pageId);
```
这个iframe是一个jq对象

<a id="5-2-4-6-%E6%A0%B9%E6%8D%AEpageid%E8%8E%B7%E5%BE%97%E5%BD%93%E5%89%8Dpanel"></a>
##### 5-2-4-6. 根据pageId获得当前panel

```
var $panel=findTabPanel(pageId)
```
这个panel是一个div，装有iframe，jq对象

<a id="5-2-4-7-%E5%85%B3%E9%97%ADtab"></a>
##### 5-2-4-7. 关闭tab

```
closeTabByPageId(pageId);
```
pageId是你创建tab时候的id. 只要知道你要操作的pageId，也可以在一个子iframe页面关闭另外一个子iframe页面。

<a id="5-2-4-8-%E5%88%B7%E6%96%B0tab"></a>
##### 5-2-4-8. 刷新tab
```
refreshTabById(pageId)
```
只要知道pageId，就可以刷新任何tab


<a id="5-2-4-9-%E6%9C%AA%E5%AE%8C%E5%BE%85%E7%BB%AD"></a>
##### 5-2-4-9. 未完待续

<a id="6-browser-support%E6%B5%8F%E8%A7%88%E5%99%A8%E6%94%AF%E6%8C%81"></a>
## 6. Browser Support(浏览器支持)

- IE 9+
- Firefox (latest)
- Chrome (latest)
- Safari (latest)
- Opera (latest)

<a id="7-license"></a>
## 7. License

AdminLTE is an open source project by [Almsaeed Studio](https://almsaeedstudio.com) that is licensed under [MIT](http://opensource.org/licenses/MIT). Almsaeed Studio

reserves the right to change the license of future releases.

(开源免费)

<a id="8-todo-list"></a>
## 8. Todo List

- jquery pace integration
- example to manager tabs within an iframe page.

<a id="9-%E7%9B%B8%E5%85%B3%E7%A4%BA%E4%BE%8B%E9%A1%B9%E7%9B%AE"></a>
## 9. 相关示例项目

- Java Web: [weituotian-video](https://gitee.com/weituotian/weituotian-video)
- More to contact me. 