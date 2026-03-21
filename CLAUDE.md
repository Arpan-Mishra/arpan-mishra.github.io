# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a fully static HTML/CSS/JavaScript portfolio website hosted on GitHub Pages. There is no build system, package manager, or compilation step — files are served directly.

## Running Locally

```bash
python3 -m http.server 8000
# Visit http://localhost:8000
```

## Deployment

Push to the `main` branch. GitHub Pages automatically deploys from the repository root.

## Architecture

Single-page scroll design in `index.html` with sections: About, Experience, Projects, Blog, Contact.

**Key files:**
- `index.html` — entire portfolio content and structure
- `css/screen.css` — all custom styles (organized into sections 0–10 per the internal TOC)
- `js/index.js` — jQuery-based interactions: scroll tracking, nav highlighting, icon replacement, alternating post styles
- `js/icons.js` — custom icon font definitions
- `404.html` — custom error page mirroring the main site's style
- `docs/resume.pdf` — downloadable resume

**Dependencies (CDN-loaded, no local install needed):**
- jQuery 1.11.3
- Font Awesome 5.12.1
- Google Fonts (Oswald, Open Sans, Roboto Slab)
- `fork-awesome/` — local copy of a Font Awesome fork

**Contact form** uses Getform.io as the backend endpoint.

## Responsive Breakpoints

Defined in `css/screen.css`:
- `≤ 600px` — mobile layout
- `≤ 1130px` — tablet/intermediate layout