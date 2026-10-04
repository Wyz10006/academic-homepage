# Wyz10006 的学术主页

网站：https://wyz10006.github.io/academic-homepage/

使用官方 [al-folio](https://github.com/alshedivat/al-folio) 模板，保留默认样式。页面为英文，包含个人介绍、博客和论文栏目。原博客 https://wyz10006.github.io/ 继续独立运行。

## 更新内容

| 内容                         | 编辑位置                     |
| ---------------------------- | ---------------------------- |
| 姓名、网站描述               | `_config.yml`                |
| 个人介绍、研究方向、头像设置 | `_pages/about.md`            |
| GitHub、邮箱等社交链接       | `_data/socials.yml`          |
| 论文列表                     | `_bibliography/papers.bib`   |
| 论文页说明                   | `_pages/publications.md`     |
| 博客文章                     | `_posts/YYYY-MM-DD-title.md` |

尚未填写的姓名、所属机构、照片和论文可按需补充。当前展示名为 Wyz10006。

在 GitHub 打开相应文件，点击编辑，修改后提交到 `main`，网站会自动重新构建并发布。

## 添加文章

在 `_posts/` 新建文件，例如 `2026-10-04-first-note.md`：

```markdown
---
layout: post
title: My first research note
date: 2026-10-04 12:00:00 +0800
description: A short summary of this note.
---

Write your article here in Markdown.
```

文件名和 `date` 请改为实际发布日期。未来日期的文章不会在当前构建中显示。

## 部署配置

- 内容分支：`main`
- Actions 工作流：`Deploy site`
- 构建结果分支：`gh-pages`
- Settings → Pages：`Deploy from a branch` → `gh-pages` → `/ (root)`
- `_config.yml`：`url: https://wyz10006.github.io`，`baseurl: /academic-homepage`

每次提交网站内容后，`Deploy site` 生成静态页面并更新 `gh-pages`，随后 GitHub Pages 发布。可在仓库的 Actions 页面查看进度。如果发布失败，先检查最新 `Deploy site` 的日志。

不要直接编辑 `gh-pages`，下一次构建会覆盖它。

## 模板与维护

本仓库不包含 al-folio 的演示文章和虚构个人资料。上游模板的 Integration tests 依赖这些演示页面，Lighthouse Badger 使用上游演示站网址及维护者密钥，因此这两项工作流仅在上游模板仓库运行；本网站继续使用实际 Jekyll 构建、格式和链接检查。

更多设置见 [自定义说明](docs/CUSTOMIZE.md) 和 [部署说明](docs/INSTALL.md)。模板许可证保留在 [LICENSE](LICENSE)。
