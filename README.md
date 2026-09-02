# Preetam Kambar — Portfolio

Personal portfolio site for Preetam Basavaraj Kambar, an aspiring Cloud & DevOps Engineer. Built as a single static page — no build tools, no framework, no dependencies to install.

**Live site:** [preetamkambar.cloud](https://preetamkambar.cloud/)

## Overview

A one-page site covering:

- Summary / hero introduction
- Work experience (Cloud & DevOps internships)
- Skills, grouped by area
- Selected projects (CI/CD pipeline, Kubernetes GitOps, self-hosted file storage) with expandable detail modals
- Certifications
- Contact / résumé download

## Tech stack

- **HTML5 / CSS3 / vanilla JavaScript** — no framework, no build step
- **Google Fonts** — DM Sans, DM Mono, Fraunces
- Structured data via `application/ld+json` (schema.org `Person`) for SEO
- Open Graph / Twitter card meta tags for link previews

## Project structure

```
.
├── index.html                    # entire site — markup, styles, and scripts
├── logo.png                      # favicon / site icon
├── profile.jpg / .webp           # profile photo (full size)
├── profile-head.jpg / .webp      # profile photo (used for OG/Twitter previews)
├── profile-sm.jpg                # profile photo (small variant)
├── resume.pdf                    # downloadable résumé
└── Preetam_Kambar_Resume.docx    # résumé source (editable)
```

## Running locally

No build step is required. Any static file server works, e.g.:

```bash
# Python
python3 -m http.server 8000

# Node
npx serve .
```

Then open `http://localhost:8000`.

## Deployment

The site is a static bundle — deploy `index.html` and the asset files as-is to any static host (e.g. Cloudflare Pages, Netlify, Vercel, GitHub Pages). Update the `canonical`, `og:url`, and `og:image` meta tags in `index.html` if the domain changes.

## Updating content

All content lives in `index.html`:

- **Projects** — grid cards live in the `#projects` section (`<article class="proj">`); full project write-ups live in the `<dialog id="dlg-...">` blocks further down the file.
- **Skills / experience / certifications** — each has its own `<section>`, identifiable by its `id` (e.g. `#credentials`).
- **Résumé** — replace `resume.pdf` and `Preetam_Kambar_Resume.docx` and update any download links pointing to them.

## Contact

- Email: pritamkambar4@gmail.com
- LinkedIn / GitHub: linked from the site header
