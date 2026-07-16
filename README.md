# Heat Alert 🌡️

**Live, global land surface temperature — straight from NASA satellites, in your browser.**

Heat Alert is a single-page web app that renders a color-coded map of Earth's land surface temperature, lets you click anywhere for a live reading, and compares up to three locations' temperature trends over time. No backend, no database, no build step — one HTML file, hosted on GitHub Pages.

**[→ Live demo](https://extremesam.github.io/heat-alert/)** 

![Heat Alert screenshot](/screenshot.png) 

---

## Features

- 🛰️ **Global LST heatmap** — daily MODIS Terra land surface temperature imagery from NASA GIBS, covering the entire planet at every zoom level
- 📅 **Time travel** — a calendar range picker plus a day-by-day slider to scrub through the satellite archive, back to May 2012
- 📍 **Click to inspect** — click anywhere on Earth for a live temperature reading, pulled from NASA POWER
- 📈 **Compare up to 3 locations** — pin multiple sites and see their temperature trends plotted together, with a 30/90/180/365-day window selector
- ⤢ **Enlarge chart** — pop the trend chart into a larger view for a closer look
- 📍 **Use my location** — jumps straight to your position via browser geolocation
- ℹ️ **About panel** — explains the data sources and how the app works, in-app

## How it works

Everything runs client-side, in the browser:

| Feature | Data source |
|---|---|
| Map heatmap layer | [NASA GIBS](https://www.earthdata.nasa.gov/eosdis/science-system-description/eosdis-components/gibs) — MODIS Terra Land Surface Temperature (Day), served as pre-rendered map tiles |
| Click-to-inspect reading & trend chart | [NASA POWER](https://power.larc.nasa.gov/) API — Earth Skin Temperature (`TS`), Agroclimatology (AG) community |
| Base map | [CARTO](https://carto.com/basemaps) dark basemap tiles |
| Map rendering | [Leaflet.js](https://leafletjs.com/) |
| Charts | [Chart.js](https://www.chartjs.org/) |

No API keys, no accounts, and no data is stored anywhere — every request goes straight from the visitor's browser to NASA's public APIs.

## Deploying your own copy

1. Fork or download this repo
2. Make sure the main file is named `index.html` at the repository root
3. In your repo, go to **Settings → Pages**, set the source to your default branch, root folder
4. Your app will be live at `https://<your-username>.github.io/<repo-name>/`

No build step, no dependencies to install — it's ready to serve as-is.

## Known limitations

- Satellite imagery has daily gaps where cloud cover blocked the pass — it's not a seamless image every single day
- LST tiles run on roughly a two-day processing delay from NASA
- MODIS LST resolution is ~1km; fine for regional/global patterns, not building-level precision

## Credits

Built by **ExtremeSam** — [github.com/extremesam](https://github.com/extremesam)

Data courtesy of NASA's Langley Research Center POWER Project and NASA EOSDIS GIBS.

## License

*(Add a license of your choice — e.g. [MIT](https://choosealicense.com/licenses/mit/) — if you want others to freely reuse this code.)*
