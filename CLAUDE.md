# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based static website for updatez.org, focused on software modernization resources. The site is built using Jekyll-Bootstrap framework with the Twitter Bootstrap theme and is hosted on GitHub Pages via the `gh-pages` branch.

## Site Architecture

### Jekyll-Bootstrap Structure
The site uses a layered template system:
- `_layouts/` contains thin wrapper files (default.html, page.html, post.html) that delegate to theme templates
- `_includes/themes/twitter/` contains the actual theme templates
- `_includes/JB/` contains Jekyll-Bootstrap helper includes for analytics, comments, tags, categories, etc.
- Theme is set to "twitter" in _layouts/default.html frontmatter

### Content Organization
- `index.md` - Main landing page
- `pages/` - Tutorial and documentation pages (overview, user_site, local_test, etc.)
- `releases/` - Binary releases (e.g., MacDependency.dmg)
- `research/` - Research notes and scratch content
- `assets/themes/twitter/` - Theme CSS and Bootstrap files

### Configuration
- `_config.yml` - Main Jekyll configuration
  - Site title: "Updatez.org - Software Modernization resources"
  - Production URL: https://updatez.org
  - Markdown processor: kramdown
  - Syntax highlighter: rouge
  - Permalink format: /:categories/:year/:month/:day/:title
  - Analytics and comments are disabled (provider: false)

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install

# Build and serve the site locally (legacy command from Rakefile)
rake preview

# Build site with Docker (matches GitHub Actions CI)
docker run -v $PWD:/srv/jekyll -v $PWD/_site:/srv/jekyll/_site jekyll/builder:latest /bin/bash -c "chmod -R 777 /srv/jekyll && jekyll build --future"

# Serve locally with Jekyll directly
bundle exec jekyll serve
```

### Content Creation (Rake tasks)
```bash
# Create a new blog post
rake post title="Post Title" [date="2025-01-15"] [tags="[tag1,tag2]"]
# Creates file: _posts/YYYY-MM-DD-post-title.md

# Create a new page
rake page name="about.html"
rake page name="tutorials/guide.md"
```

### Theme Management
```bash
# Switch to a different installed theme
rake theme:switch name="theme-name"

# Install a theme from git
rake theme:install git="https://github.com/jekyllbootstrap/theme-twitter.git"

# Package current theme
rake theme:package name="twitter"
```

## Important Details

### Markdown Files Format
All markdown content files (index.md, pages/*.md) must include YAML frontmatter:
```yaml
---
layout: page        # or 'post' for blog posts
title: "Page Title"
description: ""     # Used for meta description tag
---
```

Posts additionally require:
```yaml
---
layout: post
title: "Post Title"
description: ""
category:
tags: []
---
{% include JB/setup %}
```

### GitHub Pages Deployment
- Primary branch: `gh-pages` (used for PR targets and deployment)
- GitHub Actions workflow: `.github/workflows/jekyll-docker.yml`
  - Triggers on push/PR to `main` branch (note: workflow config doesn't match actual branch)
  - Builds site using jekyll/builder Docker image
- Custom domain: updatez.org (configured in CNAME file)

### Files Excluded from Site Build
As configured in _config.yml, these files are not published:
- .rvmrc, .rbenv-version
- ReadMe.md, Rakefile, changelog.md, License.md

### Jekyll-Bootstrap Variables
When working with templates, key variables from _config.yml:
- `{{ BASE_PATH }}` - https://updatez.org
- `{{ ASSET_PATH }}` - Auto-generated relative to BASE_PATH and theme
- `site.JB.version` - 0.3.0
