# Gotta Print 'Em All — FIT3179 Data Visualisation 2

A one-page Vega-Lite visualisation of the Pokémon Trading Card Game for the average Australian.

## Folder layout (same as the FIT3179 studio examples)

```
index.html        the page: Pure.css layout, text, and one <div> per chart
css/styles.css    page styling
js/               one Vega-Lite spec per chart (*.vg.json) + the world map TopoJSON
data/             small CSV files the charts read
sketch/           put the PDF of your hand-drawn sketch here
```

## Preview it locally

Open the folder in VS Code, right-click `index.html`, choose **Open with Live Server**.
(Opening the file by double-clicking won't load the charts; it needs Live Server or GitHub Pages.)

## Add a new chart

1. Save the spec as `js/<name>.vg.json`. Data paths start with `data/`, e.g. `"url": "data/sets_clean.csv"`.
2. In `index.html`, remove `placeholder` from the matching `<div>` and delete its text.
3. Add one line at the bottom of `index.html`:
   `vegaEmbed('#vis_s2_timeline', "js/s2_timeline.vg.json", opts).catch(console.error);`

## Editing a spec in the online Vega editor

The editor can't see your `data/` folder. While editing there, temporarily replace `data/` with your live address,
e.g. `https://<your-username>.github.io/pokemon-dv2/data/`, then change it back before saving into `js/`.

## Publish (GitHub Pages)

1. Create a **public** repository called `pokemon-dv2` on GitHub.
2. Upload everything in this folder (keep the folders).
3. Settings → Pages → Branch: `main`, folder: `/ (root)` → Save.
4. After a minute the page is live at `https://<your-username>.github.io/pokemon-dv2/`. Test it in an incognito window.
