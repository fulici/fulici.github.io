---
title: 使用 Hexo 和 GitHub Pages 搭建个人博客
date: 2026-11-01 21:00:00
tags:
  - Hexo
  - GitHub Pages
  - 教程
categories:
  - 建站
description: 从本地写作到自动部署，记录这套博客的工作方式。
---

这个博客由 Hexo 生成静态页面，再发布到 GitHub Pages。整个过程可以拆成三个部分：写作、构建和发布。

## 写作

在博客源码目录中新建文章：

```bash
npx hexo new post "文章标题"
```

随后编辑 `source/_posts` 目录中的 Markdown 文件。本地预览时运行：

```bash
npm run server
```

打开 `http://localhost:4000` 即可查看效果。

## 构建

Markdown 只是一份源文件。Hexo 会把文章、主题和站点配置合成为静态网站：

```bash
npm run build
```

构建结果位于 `public` 目录。这个目录不应该手工修改，因为下一次构建时内容会被重新生成。

## 发布

运行：

```bash
npm run deploy
```

Hexo 会将构建结果提交到 GitHub Pages 仓库。GitHub 收到新提交后会自动更新网站。

## 日常节奏

以后每次写博客，只需要完成三步：

1. 新建或编辑 Markdown 文章。
2. 本地预览并检查排版。
3. 构建、发布并访问线上地址确认。

工具应该让记录变得简单。把重复的构建和发布交给命令，把注意力留给真正想写下的内容。
