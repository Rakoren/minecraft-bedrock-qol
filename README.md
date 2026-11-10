# Site (future)

Static page, hosted free on GitHub Pages. No server.

Plan:
1. Load `modules.json`, render a checkbox per module.
2. On download, bundle the selected modules plus core into a zip in the browser (JSZip).
3. Generate `main.js` importing only the selected modules, and fill in the manifest.
4. Output a `.mcaddon` / `.mcpack`.

Pack contents are chosen at build time. Live toggles stay in the in-game settings form.

Not started. Depends on M1-M5 being stable first.
