+++
date = '2025-04-21T01:05:22+08:00'
draft = true
title = '使用hugo生成静态页面并自动部署githubPages的两个坑'
tags = ["随笔", "hugo"]
+++

这个博客是使用 hugo 本地 生成的静态页面，使用 github pages 部署的。
但是在使用 hugo 生成静态页面和 github pages 部署的过程中遇到了一些坑，记录一下。
主要是使用 chatgpt 生成的教程

教程原文不贴了

遇到的问题主要是 action 从一个仓库 复制到另一个仓库的权限问题， 需要生成key

还有就是hugo主题是使用的 github 上的主题， 但是没有使用 submodule 的方式引入， 直接下载到本地了。 这样在使用 action 的时候就会报错， 需要在 action 中添加一个步骤， 将主题文件夹复制到指定位置。
然后再使用 hugo 生成静态页面。

