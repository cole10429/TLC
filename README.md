# Tender Loving Carpentry Client Quotes

Static GitHub Pages site for client-facing Tender Loving Carpentry quote presentations.

## Live URL

Hilary Smee quote page:

```text
https://cole10429.github.io/TLC/quotes/hilary-smee/
```

## GitHub Pages setup

This repository publishes with the custom workflow at `.github/workflows/deploy-pages.yml`. The workflow uploads this static directory to GitHub Pages:

```text
docs/
```

The deployable quote files live under:

```text
docs/quotes/hilary-smee/
├── index.html
└── assets/
    ├── tlc-logo.png
    └── Hilary-Smee-Cottage-Renovation-Quote.pdf
```

## Safety notes

Only deploy the rendered HTML and public assets. Do not commit local extraction artifacts, audit reports, working document files, or email drafts.

The site includes `robots.txt` plus page-level `noindex, nofollow` metadata to discourage indexing, but GitHub Pages URLs are still publicly reachable by anyone with the link.
