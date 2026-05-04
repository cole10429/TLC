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

## Updating a quote or PDF

Avoid deleting the PDF and then uploading a replacement in a separate commit. GitHub Pages deploys every commit, so a delete-only commit can briefly publish a broken PDF link.

Preferred workflow:

1. Update `docs/quotes/hilary-smee/index.html` and `docs/quotes/hilary-smee/assets/Hilary-Smee-Cottage-Renovation-Quote.pdf` together in one commit.
2. If the PDF keeps the same filename, update the query string on the button link, for example `?v=20260504-3`, so browsers fetch the newest copy instead of using a cached one.
3. Wait for the GitHub Pages workflow to finish successfully.
4. Test the landing page and the PDF button from the live Pages URL.
