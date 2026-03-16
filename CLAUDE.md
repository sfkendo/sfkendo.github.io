# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## About This Project

Static site for the **San Francisco Kendo Dojo** (sanfranciscokendo.org), hosted on GitHub Pages using Jekyll. The site was originally restored from the Internet Archive's Wayback Machine.

## Local Development

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
bundle exec jekyll build   # output to _site/
```

## Architecture

**Jekyll layout:** All pages use `_layouts/default.html`, which renders the shared `<head>`, banner image, nav, sidebar (practice schedule), and footer. Pages supply their unique content plus front matter variables:

- `title` — `<title>` tag
- `nav_current` — which nav item gets `current_page_item` class (`home`, `join`, `instructors`, `resources`, `contact`)
- `banner_image` — absolute path to the page's banner image (e.g. `/index_files/men_1000_180.jpg`)
- `banner_alt` — alt text for the banner

**Shared include:** `_includes/enrollment-notice.html` contains the enrollment announcement shown on `index.html`, `join.html`, and `contact.html`. Update it in one place when enrollment info changes.

**Page files:** `index.html`, `join.html`, `instructors.html`, `resources.html`, `contact.html`, `covid.html` — each contains only its page-specific content with front matter.

**Static redirect files** (no front matter, not processed by Jekyll): `forms.html` → DocuSign, `schedules.html` → Google Drive.

**Assets:** Page-specific images live in `<page>_files/` directories. Shared assets (logo, CSS) are in `shared_files/`.

## Common Updates

- **Enrollment info:** Edit `_includes/enrollment-notice.html` — propagates to all three pages that show it.
- **Practice schedule:** Edit the sidebar in `_layouts/default.html`.
- **Instructor roster:** Edit `instructors.html` and add/remove photos in `instructors_files/`.
