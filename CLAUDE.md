# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal academic homepage for Julian Straub, built with Hugo (static site generator) using the "no-style-please" minimalist theme. Deployed to GitHub Pages via GitHub Actions.

## Build & Development Commands

```bash
hugo server            # Local dev server with live reload (http://localhost:1313)
hugo server -D         # Dev server including draft posts
hugo                   # Build site to public/
hugo --minify          # Production build with minification
```

Hugo extended edition is required (for SCSS processing). CI uses Hugo 0.128.0.

## Architecture

**Content model:** Posts in `content/posts/` represent research projects/papers. Each post uses this frontmatter pattern:

```yaml
---
title: "Paper Title"
img: "/images/thumbnail.png"
page: "https://link-to-project-page"
date: YYYY-MM-DD
draft: false  # set true to hide
---
```

A template exists at `content/posts/template.md`.

**Layout hierarchy:**
- `layouts/index.html` — Home page: renders profile image, bio from `content/_index.md`, and menu from `data/menu.toml`
- `layouts/posts/single.html` — Individual post pages
- `layouts/posts/list.html` — Post archive with optional year grouping
- `layouts/_default/baseof.html` — Base HTML wrapper for non-post pages
- `layouts/posts/baseof.html` — Base wrapper for posts (adds custom JS support via `custom_js` frontmatter)

**Key partials:**
- `partials/post_list.html` — Renders post cards with thumbnails and metadata
- `partials/menu_item.html` — Recursive menu rendering from `data/menu.toml`
- `partials/mathjax.html` — MathJax config; enabled per-post with `mathjax: true` in frontmatter

**Custom shortcodes:** `texd` (display math), `texi` (inline math), `details` (collapsible sections).

**Styling:** `assets/css/main.scss` — Single SCSS file handling light/dark/auto themes. Processed through Hugo Pipes with fingerprinting and SRI.

**Static assets:** Images go in `static/images/`, downloadable files (PDFs, slides) in `static/download/`.

## Deployment

Pushes to `main` trigger `.github/workflows/hugo.yaml`, which builds with `hugo --minify` and deploys to GitHub Pages. No manual deployment needed.

## Configuration

- `config.toml` — Hugo settings: syntax highlighting (rrt style), table of contents (h2-h3), auto dark mode
- `data/menu.toml` — Home page menu structure (currently shows recent posts with archive link)
