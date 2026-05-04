# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Hugo static site for an academic personal profile, using the PaperMod theme. Deployed to GitHub Pages at `https://tobiaslo.github.io/Profile/` via GitHub Actions on push to `main`.

## Development Commands

```bash
hugo server          # Start local dev server at http://localhost:1313
hugo                 # Build static site to ./public/
```

No package.json or Makefile — Hugo handles everything.

## Content Architecture

Content lives in `content/` with subdirectories per type (`papers/`, `books/`, `courses/`, `data/`). Each item is a directory with `index.md` plus associated assets (images, PDFs).

**Paper frontmatter structure** (see `archetypes/paper.md`):
```yaml
title: "Paper Title"
date: YYYY-MM-DD
url: /paper/slug
tags: ["tag1", "tag2"]
author: ["Name1", "Name2"]
cover:
    image: "filename.png"
    relative: true
editPost:
    URL: "https://doi.org/..."
    Text: "Venue Name"
```

Paper body sections: Download (links), Abstract, Figures, Citation (BibTeX).

## Theme & Layout

- **Theme**: PaperMod (git submodule at `themes/PaperMod/`)
- **Custom CSS**: `assets/css/extended/center-home.css` — centers the profile home section and header nav
- **Layout overrides**: `layouts/` directory for any PaperMod customizations
- **Static assets**: `static/` holds CV (`cv.pdf`), profile photo, favicons

## Configuration

`config.yml` is the sole Hugo config. Key settings:
- `baseURL`: `https://tobiaslo.github.io/Profile/`
- Profile mode enabled with social icons (email, Google Scholar, GitHub, LinkedIn)
- Dark theme by default, math support enabled, syntax highlighting (autumn style)
- Only "Papers" is active in the menu

## Deployment

GitHub Actions (`.github/workflows/hugo.yml`) builds with Hugo v0.153.2 + Dart Sass on push to `main` and deploys `./public/` to GitHub Pages. Timezone is set to `Europe/Oslo`.
