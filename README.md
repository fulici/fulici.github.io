# 佛狸祠的个人博客

使用 [Hexo 8](https://hexo.io/) 与 [Fluid](https://github.com/fluid-dev/hexo-theme-fluid) 主题构建，发布到 GitHub Pages。

线上地址：<https://fulici.github.io>

## 日常写作

新建文章：

```powershell
npx hexo new post "文章标题"
```

文章位于 `source/_posts`。可以按下面的命令启动本地预览，访问 `http://localhost:4000`：

```powershell
npm run server
```

## 发布

每次发布时运行：

```powershell
npm run deploy
```

该命令会清理旧构建、重新生成 `public` 目录，并把构建结果推送到 `fulici/fulici.github.io` 的 `main` 分支。

## 主要配置

- 站点标题、网址与部署仓库：`_config.yml`
- 主题、导航、首页和关于页：`_config.fluid.yml`
- 自定义样式：`source/css/custom.css`
- 文章目录：`source/_posts`
- 固定页面：`source/about/index.md`

`public`、`node_modules` 和 `.deploy_git` 均为生成目录，不需要手工编辑，也不应提交到源码仓库。
