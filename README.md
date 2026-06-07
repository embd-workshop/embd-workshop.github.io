# EMBD Workshop Proposal

Website for the proposed workshop **Experimentally-Grounded Machine Learning for Biological Discovery** (EMBD), submitted as a NeurIPS 2026 workshop proposal and focused on aligning machine learning with experimental biological and chemical discovery.

🔗 **Live site:** https://embd-workshop.github.io/

## Overview

A single-page static site — plain HTML, CSS, and a small amount of JavaScript. No build step, no dependencies. It is served directly by GitHub Pages.

```
index.html              # all page content (edit here)
assets/
  css/styles.css        # theme + layout
  js/main.js            # nav, scroll-spy, key-date logic (enhancement only)
  img/people/           # speaker & organizer headshots (square ~480px)
  img/logos/            # sponsor / venue logos
  img/favicon.svg
.nojekyll               # tells GitHub Pages to serve files as-is
```

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Editing content

All content lives in `index.html`, organized into clearly commented sections (`Hero`, `Key dates`, `News`, `About`, `Themes`, `Call for Papers`, `Program`, `Organizers`, `Community`, `Footer`).

**Add a news item** — add an `<li>` to the `.news-list` in the *News* section:

```html
<li><time datetime="2026-07">Jul 2026</time><span>Acceptance notifications sent.</span></li>
```

**Update the OpenReview link** — in the *Call for Papers* section, replace the disabled button with the live submission link when available.

**Key dates** — edit the `.date-card` blocks under *Key dates*. The `data-deadline="YYYY-MM-DD"` attribute lets the page automatically grey out past dates and flag the next upcoming one.

## Deploying to GitHub Pages

1. Push to the `main` branch of `github.com/embd-workshop/embd-workshop.github.io`.
2. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch **`main`**, folder **`/ (root)`**, then **Save**.
3. The site publishes at https://embd-workshop.github.io/ within a minute or two.

All asset paths are relative, so the site works correctly under the project root.

## License

Content © 2026 the workshop organizers. Speaker and organizer photographs remain the property of their respective owners and are used here for the purpose of the workshop program.
