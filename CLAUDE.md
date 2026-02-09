# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Kovel.ai is a static landing page for an AI business agents startup. The entire site is a single `index.html` file (HTML, CSS, and JS inlined) with no build step or dependencies.

## Deployment

Hosted on Cloudflare Pages via Wrangler. Configuration is in `wrangler.jsonc`.

```bash
# Deploy to Cloudflare
npx wrangler pages deploy ./
```

## Development

No build tools, package manager, or dev server is configured. Open `index.html` directly in a browser to preview.

## Architecture

- **Single-file site**: All markup, styles, and scripts live in `index.html`
- **Fonts**: Google Fonts (Instrument Serif, Geist Mono, DM Sans)
- **Design tokens**: CSS custom properties in `:root` (`--bg`, `--accent`, `--ember`, `--gold`, etc.)
- **Animations**: CSS keyframes for background orbs, steam particles, scroll-reveal; JS for cursor trail and randomized steam drift
- **Waitlist form**: Client-side only (no backend wired up yet) — submits are handled with a placeholder JS handler
- **Scroll reveal**: Uses `IntersectionObserver` to add `.visible` class on `.pain-section` and `.vision-section`
