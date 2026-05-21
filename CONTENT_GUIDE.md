# Personal Site Content Guide

这个站点是 Jekyll/Academic Pages 模板。日常维护时，通常只需要改下面这些文件。

## 首页 / 关于我

编辑：

```text
_pages/about.md
```

这里会生成网站首页 `/`，同时也通过 redirect 对应 `/about/`。

适合写：

- 个人简介
- 研究方向
- 当前关注的问题
- 联系方式
- 代表性经历摘要

## 顶部导航

编辑：

```text
_data/navigation.yml
```

这里控制顶部菜单显示哪些入口，以及顺序。

当前导航是：

- 关于我 -> `/about/`
- 教育背景 -> `/education/`
- 项目经历 -> `/portfolio/`
- 技能栈 -> `/skills/`

## 侧边栏头像、姓名、邮箱、链接

编辑：

```text
_config.yml
```

重点看 `author:` 这一段。这里控制左侧个人卡片，包括：

- 头像：`avatar`
- 姓名：`name`
- 简介：`bio`
- 位置：`location`
- 单位：`employer`
- 邮箱：`email`
- GitHub、Google Scholar 等外部链接

头像图片放在：

```text
images/
```

`author.avatar` 只写图片文件名即可，例如：

```yaml
avatar: "2026-05-20_204709_716.jpg"
```

## 教育背景

编辑：

```text
_pages/education.md
```

适合写本科、硕士、博士经历，以及研究方向、课程、荣誉等。

## 技能栈

编辑：

```text
_pages/skills.md
```

适合写研究技能、编程语言、工具链、写作能力等。

## 项目经历列表页

编辑：

```text
_pages/portfolio.html
```

这个文件主要控制 `/portfolio/` 页面标题和列表前的说明文字。

## 每一个具体项目

新增或编辑：

```text
_portfolio/*.md
```

现在已有：

```text
_portfolio/cpu-microarchitecture-research.md
_portfolio/cache-optimization.md
```

每个项目文件开头都需要保留 front matter，例如：

```markdown
---
title: "项目标题"
excerpt: "项目列表页显示的简短摘要。"
collection: portfolio
---

这里写项目正文。
```

适合写：

- 项目背景
- 你的贡献
- 使用工具
- 实验设计
- 结果与图表
- 相关链接

## CV

编辑：

```text
_pages/cv.md
```

如果你之后想启用简历页面，可以把 `/cv/` 加回 `_data/navigation.yml`。

如果使用 JSON 版本 CV，则编辑：

```text
_data/cv.json
```

## 论文、报告、教学、博客

当前这些栏目没有放进导航，我也已经删除了模板自带的示例内容。之后如果需要启用，可以分别新增：

```text
_publications/*.md
_talks/*.md
_teaching/*.md
_posts/*.md
```

然后再到 `_data/navigation.yml` 添加对应入口。

## 本地预览

如果本机安装了 Ruby、Bundler 和 Jekyll，可以运行：

```powershell
bundle exec jekyll serve
```

然后打开终端输出里的本地地址预览。
