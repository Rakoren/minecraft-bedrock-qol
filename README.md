# QoL Add-on Builder

**Live at https://rakoren.github.io/minecraft-bedrock-qol/**

A static page, no server: pick the features you want for a vanilla-feeling Minecraft Bedrock QoL add-on and download a custom `.mcaddon`. The pack is built in your browser. You can also open `index.html` straight from disk.

Files:
- `index.html`: the picker page. Features are tiles grouped by category, there's a share link (`#m=id,id`), you can load an old `.mcaddon` to re-pick its features, and the install steps are at the bottom.
- `builder.js`: the build logic. It generates `modules/index.js`, fills in the pack settings and version, and writes the zip.
- `bundle.js`: **generated**. It holds the pack files, the module list and `builder.js` in one classic script, so the page works on `file://`.

**Just want everything?** Grab the ready-made `.mcaddon` from [Releases](https://github.com/Rakoren/minecraft-bedrock-qol/releases/latest).

This repo is published from the add-on's source repo (`npm run publish-site` for the site, `npm run release` for releases). Don't edit it here.
