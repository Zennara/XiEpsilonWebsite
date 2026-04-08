# Kappa Sigma Xi Epsilon — Chapter Website

## Overview

This is the official public-facing website for the Xi Epsilon chapter of the Kappa Sigma Fraternity at Thiel College. It serves as a central hub for prospective members, alumni, and the campus community to learn about the chapter's membership, values, events, and philanthropic initiatives.

## Why This Exists

The chapter needed a dedicated web presence to communicate its identity, recruitment criteria, leadership structure, and ongoing service efforts — particularly its military-focused philanthropy programs. The site consolidates information that would otherwise be scattered across social media or word of mouth into a single, navigable resource.

## Tech Stack

- **HTML5 / CSS3 / Vanilla JavaScript** — all pages are static, hand-authored HTML files
- **Bootstrap 5.0.1** — responsive grid, layout, and component styling
- **Mobirise** — visual page builder used to scaffold and style the site (evidenced by `mbr-*` class conventions and `assets/mobirise/` directory)
- **Jarallax 1.12.7** — parallax scrolling effects on background images
- **countdown.js 2.6.1** — event countdown timers
- **yt-player** — embedded YouTube video support
- **Socicon** — social media icon font
- **Themify Icons** — general-purpose UI icon font
- **Devicon** — developer/technology icon font
- **Google Fonts** — Merriweather (serif headings), Jost and Open Sans (body text)

## Key Features

- Multi-page site covering membership recruitment, chapter history, leadership profiles, code of conduct, awards, news, blog, and newsletter sections
- Dedicated pages for signature philanthropy events: a 72-hour seesaw-a-thon benefiting military veterans and an annual 9/11 Stair Walk honoring first responders
- Donation page with downloadable PDF forms for the chapter endowment fund and local Reynolds VFW support
- Reynolds VFW partnership page for fundraising events including a spaghetti dinner and raffle
- Parallax hero sections with full-bleed photography
- Responsive navbar with dropdown navigation and smooth scrolling
- Open Graph and Twitter Card meta tags on every page for social sharing
- Maintenance page for graceful handling of pages under construction
- Image hash manifest (`hashes.json`) suggesting a basic asset integrity or cache-busting workflow

## Architecture

The site is entirely static with no server-side rendering, build tooling, or package manager. Each page is a self-contained HTML file at the project root that links to a shared `assets/` directory. The `assets/` folder is organized by library (`bootstrap/`, `parallax/`, `socicon/`, etc.) alongside a `theme/` subdirectory for custom overrides and a `images/` subdirectory for all media. There is no templating system; the navigation and footer are duplicated across pages.

## Installation / Getting Started

**Prerequisites:** Any static file server or modern web browser. No build step, package installation, or runtime environment is required.

**To run locally:**

```bash
# Clone the repository
git clone <repository-url>
cd XiEpsilonWebsite-main

# Option 1 — open directly in a browser
open index.html

# Option 2 — serve with Python's built-in HTTP server
python3 -m http.server 8080
# then visit http://localhost:8080

# Option 3 — serve with Node's http-server (if installed)
npx http-server . -p 8080
```

**To deploy:** Upload the entire project directory to any static hosting service (GitHub Pages, Netlify, Vercel, or a standard web host). No environment variables or server configuration are needed.
