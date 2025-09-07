# Repository Guidelines

## Project Structure & Module Organization
- Root config: `_config.yml` (Hexo), `_config.butterfly.yml` (theme), `package.json` (scripts/deps).
- Content: `source/_posts/` (Markdown posts), `source/images/` (assets), `source/tags/`, `source/categories/`, `source/link/`, `source/_data/`.
- Scaffolds: `scaffolds/` for post/page templates.
- CI/CD: `.github/workflows/gh-pages.yml` builds and publishes `public/` to GitHub Pages.

## Build, Test, and Development Commands
- `yarn install` or `npm install` — install dependencies.
- `yarn server` or `hexo server` — run local dev at `http://localhost:4000` with live reload.
- `yarn build` or `hexo generate` — build static site into `public/`.
- `yarn clean` or `hexo clean` — remove cache and generated files.
- `hexo new post "文章标题"` — create a new post from scaffold.
- `hexo new page "page-name"` — create a new page.

## Coding Style & Naming Conventions
- Language: content primarily in Chinese; UTF‑8 encoded files with trailing newline.
- Markdown: use fenced code blocks and relative links (e.g., `/images/…`). Place assets in `source/images/`.
- Front‑matter (2‑space indent) example:
  ```yaml
  ---
  title: 新文章标题
  date: 2025-08-01 12:00:00
  categories: [随笔]
  tags: [记录]
  ---
  ```
- Filenames: descriptive Chinese titles are fine; keep a date prefix for ordering if helpful (e.g., `08.01 新文章.md`).

## Testing Guidelines
- No unit test suite. Validate by:
  - Running `yarn server` and reviewing pages, navigation, search, and images.
  - Running `yarn build` to ensure a clean build with no errors.
  - Checking for broken links and missing assets in the browser console.

## Commit & Pull Request Guidelines
- Use Conventional Commits when possible: `feat: …`, `fix: …`, `docs: …`, `chore: …`.
- PRs should include: clear description, scope of change, screenshots/GIFs of local render, and linked issues (if any).
- Avoid unrelated changes to theme/config. Justify edits to `_config*.yml`.
- Do not commit secrets. The GitHub Pages workflow uses the repository’s `GITHUB_TOKEN`.

## Security & Configuration Tips
- Keep dependencies minimal; avoid large binaries. Optimize images before committing.
- Test config changes locally; ensure `public/` is generated and navigation behaves as expected.
