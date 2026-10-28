# Arrowhead Point HOA — Static Site

## Overview

This is a lightweight static website for the Arrowhead Point Homeowners Association (APHA), replacing the previous WordPress installation. Zero build dependencies, zero JavaScript runtime required.

## Structure

```
apha/
├── index.html          # Home page — hero + quick links
├── about.html          # Association history
├── board.html          # Board of Directors with bios
├── community.html      # Community resources (beach, tennis, testimonials)
├── beach-docks.html    # Beach & dock information & rules
├── buying-selling.html # HOA resale process for buyers/sellers
├── tennis.html         # Tennis Association (private sub-association)
├── news.html           # News & events announcements
├── contact.html        # Contact info and board directory
├── css/
│   └── style.css       # Single stylesheet (brand colors, responsive grid)
└── assets/             # Images and documents go here
```

## Why Static?

- **No server maintenance** — no PHP, no database, no updates, no security patches
- **Instant load** — files serve directly from any CDN or static host
- **Git-native** — every change is a commit, every change is reviewable
- **Zero cost** — free hosting on GitHub Pages, Netlify, or any S3 bucket

## Deployment

### Option 1: GitHub Pages
1. Push to `main` branch
2. Go to Settings → Pages → Source: Deploy from a branch → `main` / `root`

### Option 2: Netlify
1. Push this repo to GitHub
2. Go to app.netlify.com → New site from Git → select APHA repo
3. Auto-deploys on every push to `main`

### Option 3: Any HTTP server
Serve the root directory as static files:
```bash
python3 -m http.server 8000
```

## Editing

- Every page is a plain HTML file in the repo root
- Shared navigation is at the top of each file — update once per page
- Styles are in `css/style.css`
- No build step — edit, commit, push, live

## Assets

Add images to `assets/` and reference them as:
```html
<img src="assets/logo.png" alt="Arrowhead Point HOA">
```

## Current Content Notes

- Testimonials are live — from Robin R., Peter M., Lauren B.
- Board member bios are live with emails
- Beach & docks info includes waitlist details
- Some pages need content updates (dock fees, full rules, municipal links)
- The newsletter/calendar system needs a final approach (SharePoint, Google Calendar, etc.)
