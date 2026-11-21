# Yogendra Om — Personal Blog

A quiet space for reflections on spirituality, life, and the journey within. Built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, hosted on GitHub Pages.

**Live site:** https://yogendraom.github.io/

---

## 📦 What's in this repository

| Folder / File | Purpose |
|---------------|---------|
| `hugo.yaml` | Site configuration (title, menus, theme params, etc.) |
| `content/about/` | Your About page |
| `content/post/` | Your blog posts (one Markdown file per post) |
| `archetypes/post.md` | Front-matter template for new posts |
| `themes/papermod/` | The PaperMod theme (cloned submodule-style) |
| `docs/` | Built site — this is what GitHub Pages serves |
| `.gitignore` | Ignores local Hugo build artifacts |

> ⚠️ This repository is **private**. Only the published website at `yogendraom.github.io` is public.

---

## 🛠️ Prerequisites

You need **Hugo Extended** installed on your machine to build and preview locally.

### If Hugo is not installed

On macOS (Apple Silicon), you can download the latest release from https://github.com/gohugoio/hugo/releases and place the `hugo` binary in `~/bin`, then add `~/bin` to your PATH in `~/.zshrc`:

```zsh
export PATH="$HOME/bin:$PATH"
```

Verify it works:

```bash
hugo version
```

---

## ✍️ Writing a New Blog Post

### 1. Create a new post (draft)

Run this from the repository root:

```bash
hugo new post/my-reflection-title.md
```

This uses `archetypes/post.md` as a template and creates:

```markdown
---
title: "My Reflection Title"
date: 2026-11-21
draft: true
tags: []
categories: []
description: ""
---
```

### 2. Edit the post

Open `content/post/my-reflection-title.md` and write your content in Markdown. Key front-matter fields:

| Field | Description | Example |
|-------|-------------|---------|
| `title` | Post title | `"Beginning Here"` |
| `date` | Publication date | `2026-11-21` |
| `draft` | Set to `false` when ready to publish | `true` / `false` |
| `tags` | Tags for taxonomy pages | `["spirituality", "beginnings"]` |
| `categories` | Categories for taxonomy pages | `["reflections"]` |
| `description` | Short summary for listing pages | `"Why I started this space..."` |

### 3. Preview locally

Start the Hugo development server:

```bash
hugo server
```

Then open http://localhost:1313/ in your browser. The site auto-reloads as you edit.

> Posts with `draft: true` will only appear when running `hugo server --buildDrafts` or `hugo server -D`. They will **not** be included in the production build.

### 4. Build for production

When your post is ready (set `draft: false`), build the static site:

```bash
hugo --minify
```

This generates the final HTML into the `docs/` folder.

### 5. Publish

Commit and push to GitHub. GitHub Pages will automatically redeploy the site.

```bash
git add -A
git commit -m "New post: my-reflection-title"
git push origin main
```

Your site will be live at https://yogendraom.github.io/ within a minute or two.

---

## 📁 Full Publishing Checklist

```
[ ] hugo new post/my-title.md          # Create draft
[ ] Edit content/post/my-title.md      # Write content
[ ] Set draft: false in front-matter   # Mark as ready
[ ] hugo server                        # Preview locally
[ ] hugo --minify                      # Build production site
[ ] git add -A                         # Stage changes
[ ] git commit -m "..."                # Commit
[ ] git push origin main               # Deploy to GitHub Pages
```

---

## 🎨 Customizing the Site

### Site configuration (`hugo.yaml`)

Edit `hugo.yaml` to change:

- `title` — Site name shown in the header
- `params.description` — Meta description
- `params.author` — Author name
- `params.homeInfoParams` — Homepage welcome text
- `menu.main` — Navigation links (About, Archive, Search)
- `params.socialIcons` — Social media links

### Theme

The site uses [PaperMod](https://github.com/adityatelange/hugo-PaperMod), cloned into `themes/papermod/`. You can override any theme layout by creating a file with the same path under `layouts/` in your repo root.

### Adding an image to a post

Place images in `content/post/my-title/` and reference them relatively:

```markdown
![A quiet morning](./my-title/image.jpg)
```

---

## 🔐 Repository Privacy

This repository is **private** — your source code, drafts, and config are not visible to the public. Only the built website at `yogendraom.github.io` is publicly accessible.

If you ever want to change this, go to **Settings → General → Danger Zone → Change repository visibility** on GitHub.

---

## 🚀 Deployment Details

- **Host:** GitHub Pages (user site)
- **Source branch:** `main`
- **Source folder:** `/docs`
- **Build command:** `hugo --minify` (run locally, `docs/` is committed)
- **Live URL:** https://yogendraom.github.io/

---

## 📝 Example: Your First Post

Your first post is already created at `content/post/my-first-reflection.md` as a template you can reference.

Happy writing! May this space be a small shelter for your thoughts. 🌿