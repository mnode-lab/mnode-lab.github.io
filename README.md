# μNode Lab Website

Replicating DeepSeek V3 limits on consumer hardware.

## 网站地址

https://mnode-lab.github.io

## 技术栈

- **静态站点生成器**: Jekyll 4.4.1
- **托管平台**: GitHub Pages
- **主题风格**: Terminal/Hacker 风格（自定义）

## 本地开发

### 安装依赖

```bash
# 安装 Ruby 和 Jekyll
sudo apt-get install ruby-full build-essential zlib1g-dev
sudo gem install jekyll bundler

# 安装项目依赖
sudo gem install jekyll-paginate jekyll-feed jekyll-seo-tag
```

### 本地预览

```bash
# 构建站点
jekyll build

# 启动本地服务器
jekyll serve --host 0.0.0.0 --port 4000

# 访问 http://localhost:4000
```

## 发布新文章

### 1. 创建文章文件

在 `_posts/` 目录下创建新文件，文件名格式为：

```
YYYY-MM-DD-title-slug.md
```

例如：`2026-01-15-new-experiment-results.md`

### 2. 添加 Front Matter

每篇文章开头必须包含 YAML 格式的元数据：

```yaml
---
layout: post
title: "文章标题"
date: 2026-01-15 10:00:00 +0800
author: "μNode Lab"
categories: [category1, category2]
tags: [tag1, tag2, tag3]
featured: false  # 设置为 true 可置顶显示
excerpt: "文章摘要，显示在列表页"
---
```

### 3. 撰写正文

使用 Markdown 格式撰写文章内容。支持：

- 标题（`##`, `###`）
- 列表（有序、无序）
- 代码块（使用三个反引号）
- 表格
- 图片
- 链接
- 引用（`>`）

### 4. 推送到 GitHub

```bash
git add .
git commit -m "Add new post: 文章标题"
git push origin main
```

GitHub Pages 会自动构建并部署更新后的网站。

## 文章分类说明

| 分类 | 用途 |
|------|------|
| `analysis` | 技术报告深度拆解 |
| `engineering-log` | 每周更新的构建进展 |
| `hardware` | BOM 清单、选型逻辑、测试数据 |
| `software` | 代码架构、踩坑经验 |
| `benchmark` | 性能测试、Dashboard 更新 |

## 目录结构

```
mnode-lab.github.io/
├── _config.yml          # Jekyll 配置
├── _layouts/            # 页面布局模板
│   ├── default.html     # 基础布局
│   ├── home.html        # 首页布局
│   └── post.html        # 文章详情页布局
├── _includes/           # 可复用组件
│   ├── header.html      # 头部
│   └── footer.html      # 页脚
├── _posts/              # 博客文章（Markdown）
│   └── YYYY-MM-DD-title.md
├── assets/              # 静态资源
│   ├── css/
│   │   └── main.css     # 终端风格样式
│   └── js/
├── index.html           # 首页
├── about.html           # 关于页面
└── README.md            # 本文档
```

## 设计风格

网站采用 Terminal/Hacker 风格，配色方案：

- 背景色：`#0d1117` (GitHub Dark Mode 黑色)
- 主文本：`#c9d1d9` (GitHub 文本白色)
- 提示符：`#2da44e` (GitHub 绿色)
- 高亮/链接：`#58a6ff` (GitHub 蓝色)
- 次要文本：`#8b949e` (灰色)

## 注意事项

1. **文章日期不能是未来时间**，否则 Jekyll 会跳过该文章
2. **Front Matter 必须正确**，YAML 格式错误会导致构建失败
3. **文件名和日期要一致**，文件名中的日期应与 Front Matter 中的日期匹配
4. **推送前先本地测试**，确保 `jekyll build` 没有错误

## 联系方式

- GitHub: https://github.com/mnode-lab
- X (Twitter): https://x.com/MnodeLabs
- Reddit: https://reddit.com/u/mnode_lab

---

© 2026 μNode Lab | Built with Jekyll
