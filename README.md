# Austin’s website

One repository, two independently editable static websites.

| URL | Files | Purpose |
| --- | --- | --- |
| `/` | `index.html`, `style.css` | Version chooser |
| `/coded/` | `coded/` | Austin’s handwritten website, migrated from the original site |
| `/ai/` | `ai/` | AI-assisted website |
| `/shared/` | `shared/` | Assets used by both versions |

Both versions include home, about, projects, and blog pages. The header switch links to the corresponding page in the other version. Each version owns its HTML and CSS; no JavaScript or build step is required. The original site’s page content is retained in `coded/`, with navigation, document metadata, and malformed list markup repaired for the migration.

## Local preview

From this repository’s root:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000/. Serve the repository root, since navigation uses root-relative URLs.

## Editing

- Work in `coded/` for the handwritten version and `ai/` for the AI-assisted version.
- Keep version-specific styles and scripts in that version’s folder.
- Put genuinely shared assets in `shared/`. Written content is currently maintained separately; no content pipeline is needed for this small site.
- When adding a page, add the matching page to both versions or point its version switch at the other version’s homepage until a counterpart exists.
- The legacy `/about/`, `/projects/`, and `/blog/` pages redirect to the corresponding handwritten pages. Keep these redirects for existing links.

## Hosting

This layout targets the repository’s existing `01sua.github.io` root URL (or a custom domain). GitHub Pages can publish it directly from the repository root. No new hosting service, dependency installation, or deployment pipeline is required. If hosting under a project subpath later, update root-relative URLs to include that prefix.
