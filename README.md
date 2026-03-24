# Yaahua 的博客

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://yaahua.github.io/blogyaahua/)
[![Hugo](https://img.shields.io/badge/Hugo-v0.120%2B-ff4088)](https://gohugo.io/)
[![Theme](https://img.shields.io/badge/Theme-Stack-blue)](https://github.com/CaiJimmy/hugo-theme-stack)

基于 [Hugo](https://gohugo.io/) 与 [Stack](https://github.com/CaiJimmy/hugo-theme-stack) 主题构建的個人博客，部署於 GitHub Pages。

**在线访问**: https://yaahua.github.io/blogyaahua/

---

## 技术栈

- **静态生成器**: Hugo (Extended 版本)
- **主题**: Stack (深度定制：宋体、圆角设计、极简风格)
- **部署**: GitHub Actions → GitHub Pages
- **语言**: 繁体中文 (zh-tw)

## 目录结构

    ├── .github/workflows/    # GitHub Actions 部署配置
    ├── archetypes/           # 文章模板
    ├── assets/               # 样式与脚本资源
    ├── content/              # 文章内容
    │   ├── _index.md         # 首页内容
    │   ├── page/             # 独立页面（关于我等）
    │   └── post/             # 文章目录
    │       ├── 反思/         # 反思类文章
    │       ├── 日記/         # 日记类文章
    │       ├── 學史雜記/     # 学术笔记
    │       └── 創作/         # 创作类文章
    ├── static/               # 静态资源（图片等）
    ├── hugo.toml             # Hugo 配置文件
    └── README.md             # 本文件

## 本地开发

### 前置需求

- [Hugo Extended](https://gohugo.io/installation/) (v0.120.0 或更高)
- Git

### 本地预览

    # 克隆仓库
    git clone https://github.com/Yaahua/blogyaahua.git
    cd blogyaahua

    # 启动开发服务器
    hugo server -D

    # 访问 http://localhost:1313/blogyaahua/

## 写作指南

### 1. 创建新文章

在对应分类文件夹下创建新文件夹和 `index.md`：

    # 示例：创建一篇反思文章
    mkdir content/post/反思/my-new-post
    touch content/post/反思/my-new-post/index.md

### 2. Front Matter 格式

    ---
    title: "文章标题"
    description: "简短描述"
    date: 2026-03-24
    categories:
        - 反思
    tags:
        - 标签1
        - 标签2
    slug: "my-new-post"
    ---

    这里开始写正文...

### 3. 发布

    git add .
    git commit -m "Add new post"
    git push origin main

GitHub Actions 会自动构建并在几分钟内部署到网站。

## 定制化特性

- **字体**: 全局使用宋体系列（Songti、SimSun），提升文艺感
- **视觉**: 柔和浅灰白背景，大量圆角设计（border-radius）
- **功能**: 完整配置搜索、归档、标签云
- **链接**: 文章 permalink 格式为 `/p/:slug/`

## 部署状态

查看部署状态：[![GitHub Actions](https://github.com/Yaahua/blogyaahua/actions/workflows/hugo.yml/badge.svg)](https://github.com/Yaahua/blogyaahua/actions)

---

© 2026 Yaahua. 使用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 协议授权。
