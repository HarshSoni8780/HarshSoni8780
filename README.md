<div align="center">

# harsh-portfolio

**A backend engineer's portfolio, designed as a systems dashboard instead of a resume.**

[![Deployed on Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

[Live Demo](#) · [Report Bug](../../issues) · [Request Feature](../../issues)

</div>

---

## Overview

This is my personal portfolio — built to read like the systems I actually work on: a status board, not a brochure. Identity stats render as service-health metrics, navigation is styled as API routes (`GET /projects`), and each project is walked through as a **problem → decision → tradeoff → result** log instead of a flat bullet list, because that's how I'd actually explain it in an interview.

No framework, no build step. One `index.html`, deployable anywhere static hosting exists.

## Preview

<div align="center">
<img src="./screenshot.png" alt="Portfolio preview" width="800"/>
<br/><sub>Replace with an actual screenshot before publishing.</sub>
</div>

## Tech Stack

| Layer | Choice | Why |
|---|---|---|
| Markup | Semantic HTML5 | No framework overhead for a single static page |
| Styling | CSS3 (custom properties, CSS Grid) | Full control over the design tokens, zero build step |
| Typography | [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) + [IBM Plex Sans](https://fonts.google.com/specimen/IBM+Plex+Sans) | Same foundry, deliberate pairing — mono carries the "systems" identity, sans stays readable |
| Interactivity | Vanilla JS | `IntersectionObserver` for scroll reveals, no dependencies |
| Hosting | [Vercel](https://vercel.com) | Zero-config static deploy, instant preview URLs on every push |

**Design principles:**
- 🖥️ Terminal-window chrome and a CRT scanline overlay for texture without noise
- 📊 Project write-ups as an "exchange log" — the actual reasoning trail, not just outcomes
- ⌨️ Syntax-highlighted code excerpts pulled from the real implementation logic
- ♿ Respects `prefers-reduced-motion`, visible focus states, responsive to 360px

## Getting Started

No dependencies, no `npm install`. Clone and open.

```bash
git clone https://github.com/<your-username>/harsh-portfolio.git
cd harsh-portfolio
open index.html   # or just double-click it
```

For local dev with live reload, any static server works:

```bash
npx serve .
# or
python3 -m http.server 5500
```

## Deployment

### Option A — Vercel dashboard (fastest)
1. [vercel.com/new](https://vercel.com/new) → **Deploy without Git** → drag in this folder.
2. Vercel detects it as a static site. Done.

### Option B — Git-connected (recommended, auto-deploys on push)
1. Push this repo to GitHub.
2. Vercel → **New Project** → import the repo.
3. Framework preset: **Other**. Deploy.
4. Every `git push` to `main` redeploys automatically; PRs get preview URLs.

### Option C — Vercel CLI
```bash
npm i -g vercel
vercel        # preview deploy
vercel --prod # production deploy
```

## Project Structure

```
harsh-portfolio/
├── index.html      # entire site — markup, styles, and script in one file
├── README.md
└── LICENSE
```

## Before You Deploy — Checklist

- [ ] Swap placeholder `href="#"` links for real GitHub / LinkedIn / Codolio URLs
- [ ] Point the "Download resume" button at a hosted PDF (or remove it)
- [ ] Add a real screenshot and update the preview image path above
- [ ] Set a custom domain in Vercel → Project → Domains

## Roadmap

- [ ] Pull pinned GitHub repos live via the GitHub API instead of static project cards
- [ ] Add a `/blog` route for write-ups on distributed systems problems
- [ ] Lighthouse pass — target 100/100/100/100

## Author

**Harsh Soni** — Backend & Distributed Systems Engineer, VGEC Ahmedabad
📧 [harshdsoni2021@gmail.com](mailto:harshdsoni2021@gmail.com)

## License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for details.

---

<div align="center">
<sub>Built with intent, not a template.</sub>
</div>
