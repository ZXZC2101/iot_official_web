# Repository Guidelines

## Project Structure & Module Organization
This repository is a small PHP site with static assets and no build step. Entry pages live at the root: `index.php` for the homepage and `project_show.php` for the project listing page. Shared styles are in `css/`, web fonts are in `font/`, images and logos are in `img/`, and the bundled jQuery library is in `js/jQuery/`. The `server/` and `source/` directories are currently unused in application logic and should not be treated as active modules unless new code is added intentionally.

## Build, Test, and Development Commands
There is no package manager or compiled build pipeline in this project. Use PHP's built-in server for local development:

```bash
php -S localhost:8000
```

Run the command from the repository root, then open `http://localhost:8000/index.php`. For quick checks, validate syntax before committing:

```bash
php -l index.php
php -l project_show.php
```

## Coding Style & Naming Conventions
Follow the existing style: 4-space indentation in PHP, HTML, and CSS. Keep page structure simple and favor static includes over introducing frameworks. Preserve the current naming pattern for assets and stylesheets: lowercase file names, underscore-separated PHP pages (`project_show.php`), and concise CSS class names grouped by page section such as `.nav`, `.banner_box`, and `.item_show`. Do not replace bundled vendor files like `js/jQuery/jquery-3.6.0.min.js`; add custom scripts in a separate file if needed.

## Testing Guidelines
This repository does not include an automated test suite yet. Minimum validation for each change is manual browser testing on the affected page and `php -l` on edited PHP files. When updating layout or assets, verify both `index.php` and `project_show.php` still load correctly and that image/font paths remain relative to the repository root.

## Commit & Pull Request Guidelines
Git history is not available in this checkout, so use a simple, consistent commit format such as `feat: update homepage banner` or `fix: correct logo path`. Keep commits focused on one change. Pull requests should include a short summary, impacted pages or folders, manual test notes, and screenshots for any visual update.

## Security & Content Notes
Do not commit secrets, API keys, or environment-specific URLs. Optimize large replacement images before adding them under `img/`, and keep file paths stable because pages reference assets directly with relative links.
