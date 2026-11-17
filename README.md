# AutoCompare
Static site: HTML, CSS, vanilla JS, `data/cars.json`. No backend.

## Run locally
The site loads `data/cars.json` with fetch, so use a local server (not double-click):
1. `cd autocompare`
2. `python -m http.server 8000`
3. Open http://localhost:8000

## Deploy on GitHub Pages
1. Create a repo and upload the contents of this folder (index.html at the repo root).
2. Settings > Pages > Deploy from a branch > `main` / root > Save.
3. Open the URL GitHub shows (all links are relative, so project sites work).

## Images
No car photos are bundled. Add your own (licensed) images:
- Cars: `assets/images/cars/<car-id>.jpg` and `<car-id>-2.jpg` (IDs are in `data/cars.json`, e.g. `mahindra-thar-roxx`)
- Hero banner (optional): `assets/images/banners/hero.jpg`
Missing images show a placeholder automatically.

## Edit cars
Add or edit entries in `data/cars.json`. Keep `priceLakh` numeric (1 Crore = 100). All data is unverified sample data.

## Verified-only fields
`power`, `torque`, `dimensions` (length, width, height, wheelbase) and `safety` (rating, airbags) are `null` for every car. Add a value only after checking it with the manufacturer; the Compare tabs show "Not Available" for null fields.
