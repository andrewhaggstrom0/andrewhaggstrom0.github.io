# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-page personal portfolio site for an ML Engineer / Roboticist. The entire site is a single `index.html` file containing inline CSS and static HTML — no build tools, no JavaScript, no frameworks.

## Architecture

- **index.html**: Self-contained page with all styles in a `<style>` block and semantic HTML sections (Projects, About, Skills, Experience, Contact)
- Layout uses CSS Grid with a sticky sidebar (280px) + main content area, responsive at 900px and 600px breakpoints
- Design system uses CSS custom properties (`:root` vars) for colors, fonts, and category theming (ML=green, Robotics=purple, Data=orange)
- Styled after the "Minimal Mistakes" Jekyll theme aesthetic but is pure static HTML

## Development

No build step. Open `index.html` directly in a browser or serve with any static file server:

```
python3 -m http.server 8000
```

## Key Patterns

- Project cards use category-specific color classes: `atag-ml`, `atag-robot`, `atag-data` with corresponding `cat-dot-*` variants
- Contact form is front-end only (no backend wired up) — placeholder markup
- All placeholder content uses "Your Name", "yourusername", etc. — meant to be customized
