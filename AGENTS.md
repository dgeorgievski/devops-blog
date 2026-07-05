# Repository Guidelines

## Project Structure & Module Organization

This repository is a Hugo-powered personal DevSecOps and AI blog. Site configuration lives in `hugo.toml` and `config.toml`; both currently contain the same active settings, while `old-config.toml` is retained for reference. Blog content is under `content/posts/`, the about page is under `content/about/`, and new-content defaults are defined in `archetypes/default.md`. The configured theme is Blowfish at `themes/blowfish`, installed as a Git submodule.

## Build, Test, and Development Commands

- `hugo server --disableFastRender`: run the local development server with full rebuilds while editing posts or config.
- `hugo`: build the static site into Hugo's default `public/` output directory.
- `hugo --gc --minify`: produce a cleaner production build with generated asset cleanup and minification.
- `hugo new content/posts/my-post.md`: create a draft post from the default archetype.

Use Hugo Extended. Blowfish is pinned to a release that builds with Hugo `0.155.3`; upgrade Hugo and the submodule together when moving to newer Blowfish releases.

## Coding Style & Naming Conventions

Use Markdown for content and TOML for configuration. Keep front matter in YAML format, as existing posts do, with fields such as `title`, `linktitle`, `date`, `draft`, and `tags`. Name post files with lowercase kebab-case, for example `content/posts/whats-devops.md`. Prefer short paragraphs, descriptive headings, and links with meaningful text. When changing shared site settings or Blowfish parameters, update both `hugo.toml` and `config.toml` unless the project intentionally drops one of them.

## Testing Guidelines

There is no automated test suite in this repository. Treat `hugo` as the primary validation step: it should complete without errors before a change is submitted. For content edits, also run `hugo server --disableFastRender` and review affected pages, tag pages, navigation, and summaries in a browser.

## Commit & Pull Request Guidelines

Recent commits use short, direct messages such as `switched to kiera theme and fixed outdated config issues` and `Added twitter link`. Follow that style: concise, descriptive, and focused on one change. Pull requests should explain the purpose of the change, list affected pages or configuration files, mention local validation performed, and include screenshots when visual output changes.

## Security & Configuration Tips

Do not commit generated `public/` output unless deployment explicitly requires it. Avoid adding secrets, analytics tokens, or third-party service keys directly to TOML files; document required configuration instead.
