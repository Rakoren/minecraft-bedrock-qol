# Site

Static page, no server: pick features, download a custom `.mcaddon`. Hosts free on GitHub Pages, or just open `index.html` from disk.

Files:
- `index.html`: the page (one checkbox per module from `modules.json`, pack version box, download button).
- `builder.js`: the build logic (generate `modules/index.js`, set the manifest version, write a zip). Shared with `tools/gen-index.mjs`, so the site and the CLI always generate the same index.
- `bundle.js`: **generated** by `npm run site` (pack files + modules.json + builder.js in one classic script, so it works on file:// where browsers block module imports). Commit it so Pages can serve it.

After changing any pack file or `modules.json`, run `npm run site` and commit `bundle.js`.

Pack contents are chosen at build time; live toggles stay in the in-game settings form. Dev modules (`"dev": true`, like `hello`) are never offered.
