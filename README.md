# μNode Lab Website

Replicating DeepSeek V3 limits on consumer hardware.

## Website

https://mnode-lab.github.io

## Tech Stack

- **Static Site Generator**: Jekyll 4.4.1
- **Hosting**: GitHub Pages
- **Theme**: Custom Terminal/Hacker Style

## Local Development

### Install Dependencies

```bash
# Install Ruby and Jekyll
sudo apt-get install ruby-full build-essential zlib1g-dev
sudo gem install jekyll bundler

# Install project dependencies
sudo gem install jekyll-paginate jekyll-feed jekyll-seo-tag
```

### Local Preview

```bash
# Build site
jekyll build

# Start local server
jekyll serve --host 0.0.0.0 --port 4000

# Visit http://localhost:4000
```

## Publishing New Posts

### 1. Create Post File

Create a new file in `_posts/` directory with the format:

```
YYYY-MM-DD-title-slug.md
```

Example: `2026-01-15-new-experiment-results.md`

### 2. Add Front Matter

Each post must include YAML front matter:

```yaml
---
layout: post
title: "Post Title"
date: 2026-01-15 10:00:00 +0800
author: "μNode Lab"
categories: [category1, category2]
tags: [tag1, tag2, tag3]
featured: false  # Set to true for pinned display
excerpt: "Post excerpt shown in list view"
---
```

### 3. Write Content

Write content in Markdown format. Supports:

- Headers (`##`, `###`)
- Lists (ordered, unordered)
- Code blocks (use triple backticks)
- Tables
- Images
- Links
- Blockquotes (`>`)

### 4. Push to GitHub

```bash
git add .
git commit -m "Add new post: Post Title"
git push origin main
```

GitHub Pages will automatically build and deploy the updated site.

## Post Categories

| Category | Purpose |
|----------|---------|
| `analysis` | In-depth technical analysis |
| `engineering-log` | Weekly build progress updates |
| `hardware` | BOM lists, hardware selection, test data |
| `software` | Code architecture, debugging experiences |
| `benchmark` | Performance tests, dashboard updates |

## Directory Structure

```
mnode-lab.github.io/
├── _config.yml          # Jekyll configuration
├── _layouts/            # Page layout templates
│   ├── default.html     # Base layout
│   ├── home.html        # Home page layout
│   └── post.html        # Post detail page layout
├── _includes/           # Reusable components
│   ├── header.html      # Header
│   └── footer.html      # Footer
├── _posts/              # Blog posts (Markdown)
│   └── YYYY-MM-DD-title.md
├── assets/              # Static assets
│   ├── css/
│   │   └── main.css     # Terminal style CSS
│   └── js/
├── index.html           # Home page
├── about.html           # About page
└── README.md            # This document
```

## Design Style

Terminal/Hacker style with color scheme:

- Background: `#0d1117` (GitHub Dark Mode black)
- Main text: `#c9d1d9` (GitHub text white)
- Prompt: `#2da44e` (GitHub green)
- Highlight/Links: `#58a6ff` (GitHub blue)
- Secondary text: `#8b949e` (Gray)

## Important Notes

1. **Post dates cannot be in the future** - Jekyll will skip future-dated posts
2. **Front Matter must be correct** - YAML format errors will cause build failures
3. **Filename and date must match** - Date in filename should match Front Matter date
4. **Test locally before pushing** - Ensure `jekyll build` runs without errors

## Contact

- GitHub: https://github.com/mnode-lab
- X (Twitter): https://x.com/MnodeLabs
- Reddit: https://reddit.com/u/mnode_lab

---

© 2026 μNode Lab | Built with Jekyll
