# jquery.doc.toc.js
根据文章内标题自动生成目录的jquery插件

## Contents 目录

- [Introduction 介绍](#introduction-介绍)
- [Demo 演示](#demo-演示)
- [Docs 文档](#docs-文档)
- [License 许可证](#license-许可证)

## Introduction 介绍

jquery.doc.toc.js是一款简单、轻量的TOC插件，是在jquery.titleNav.js的基础上进行了修改，主要增加了动态获取TOC距离顶部和左侧或者右侧的距离的功能。

## Demo 演示

[行风'S Blog](https://acme.top/2018/10/03/typesetting-demo/)

## Docs 文档

```javascript

  // 初始化文章目录
  $('article').docToc({
    // 活动状态发生改变时的事件
    // @param elements 文章标题对象集合
    // @param active_element 活动的文章标题对象
    activeChange: function (elements, active_element) {
      // 标题活动状态改变后可以做一些额外的样式处理
      $(elements).css("cssText", "color: #2f2f2f; border-left-color: #cacaca;");
      $(active_element).css("cssText", "color: " + theme_color + " !important; border-left-color: " + theme_color + " !important;");
    },
    // 动态获取固定位置是距离顶部的位置
    getFixedTop: function () {
      return 10;
    },
    // 动态获取距离顶部的距离
    getTop: function () {
      return 10;
    },
    // 动态获取距离左侧的距离
    getLeft: function () {
      return 200;
    }
  });

```

## License 许可证

<a href="https://github.com/acme-top/jquery.doc.toc.js/master/LICENSE"><img alt="License" src="https://img.shields.io/badge/license-MIT License-orange.svg?style=flat-square"/></a>

Open sourced under the MIT license.

根据 MIT 许可证开源。
