# Website editing boundaries

This repository contains two independently maintained versions of Austin’s website.

- Default AI implementation and design work to `ai/`.
- Treat `coded/` as Austin’s handwritten work. Do not change its HTML, CSS, or JavaScript unless the user explicitly requests edits there or authorizes a refactor that affects it.
- Root landing-page files, legacy redirects, documentation, and `shared/` are common infrastructure. Change them when relevant to the user’s request.
- Keep each version’s styles and scripts independent. Share assets only when useful.
- Keep the version switch on every content page. Link to the equivalent page in the other version, or its homepage if no equivalent exists.
- Preserve legacy redirects and verify local links after moving pages.
- Keep the site compatible with static GitHub Pages hosting; do not add a build system or dependencies without a concrete need.
