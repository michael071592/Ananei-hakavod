# AGENTS.md

## Cursor Cloud specific instructions

### Repository overview

This is the **Ananei-hakavod / ACLIMOR** repository — a static HTML landing page for an industrial chiller/HVAC service company (aclimor.co.il). The site is in Hebrew (RTL) with no build system, no package manager, and no dependencies.

### Branches

- `main` — contains only `README.md` and a PDF document.
- `codex/create-professional-pdf-proposal-for-aclimor` — contains the static `index.html` landing page (625 lines, vanilla HTML/CSS, Google Fonts via CDN).

### How to serve the application

There is no build step. Serve any branch containing `index.html` with a static file server:

```bash
python3 -m http.server 8080
# or
npx serve -p 8080
```

### Lint / Test / Build

- **No linter** is configured (no ESLint, Prettier, or similar).
- **No automated tests** exist.
- **No build step** is required — the HTML is self-contained with inline CSS.

### Non-obvious notes

- The landing page uses `print-color-adjust: exact` CSS for PDF printing fidelity — backgrounds and gradients are preserved when printing.
- Google Fonts (`Assistant`) is loaded from CDN; an internet connection is required for proper font rendering.
- The page is fully RTL Hebrew — `dir="rtl"` and `lang="he"` are set on the `<html>` element.
