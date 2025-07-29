# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hexo-based blog website using the Butterfly theme. The blog is authored by 优弧 (itcodes) and contains Chinese content focused on technology and personal reflections. The site is deployed to GitHub Pages automatically via GitHub Actions.

## Key Commands

### Development Commands
- `yarn install` - Install dependencies
- `yarn server` or `hexo server` - Start local development server
- `yarn clean` or `hexo clean` - Clean generated files
- `yarn build` or `hexo generate` - Build static site for production
- `yarn deploy` or `hexo deploy` - Deploy site (configured but not used, deployment is via GitHub Actions)

### Content Management
- `hexo new post "Title"` - Create a new blog post
- `hexo new page "page-name"` - Create a new page
- `hexo new draft "Title"` - Create a new draft post

## Architecture

### Directory Structure
- `source/_posts/` - Blog post markdown files (Chinese content)
- `source/_data/` - Data files including `link.yml` for friend links
- `source/categories/`, `source/tags/`, `source/link/` - Special pages
- `scaffolds/` - Templates for new posts, pages, and drafts
- `_config.yml` - Main Hexo configuration
- `_config.butterfly.yml` - Butterfly theme configuration
- `package.json` - Node.js dependencies and scripts

### Theme Configuration
The site uses the Butterfly theme (hexo-theme-butterfly) with extensive customization:
- Chinese language (zh-CN) with Traditional/Simplified conversion
- Live2D character (Miku model) 
- Giscus comments system
- Various visual effects (fireworks, ribbons, typing effects)
- Dark/light mode support
- Social sharing and analytics ready

### Deployment
- GitHub Actions workflow in `.github/workflows/gh-pages.yml`
- Automatic deployment on push to main branch
- Uses `yarn install` and `yarn build` commands
- Deploys to GitHub Pages from `./public` directory

### Dependencies
Key dependencies include:
- Hexo 6.3.0 static site generator
- Multiple Hexo plugins for feeds, search, sitemap, etc.
- Butterfly theme with Live2D integration
- Various utility packages for enhanced functionality

### Content Language and Style
- Primary language: Chinese (zh-CN)
- Blog posts are personal reflections and technical articles
- File naming uses Chinese characters and dates (e.g., "05.11 养驴的经验.md")
- Author uses pen name "优弧" with motto "但行好事，莫问前程"