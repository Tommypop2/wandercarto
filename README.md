# Wandercarto

Turn GPX files from a ride, hike, run, or paddle into a minimalist,
print-ready poster — a route map over hillshaded terrain, a real
elevation profile, and roads and place names drawn from OpenStreetMap.

No install, no account, no build step, no dependencies. It's a single
self-contained HTML file that runs entirely in your browser.

## Try it

- **Online:** **[rlschroeder.github.io/wandercarto](https://rlschroeder.github.io/wandercarto/)** — just open it, no download needed
- **Locally:** download [`index.html`](index.html) (or clone the repo) and open it directly in a browser

## Features

- Drag-and-drop any number of GPX files — sorted automatically by date/time
- Real elevation profile pulled straight from your GPX data
- Hillshaded terrain from [AWS Open Data terrain tiles](https://registry.opendata.aws/terrain-tiles/) (3DEP / SRTM / GMTED)
- Roads and place names from [OpenFreeMap](https://openfreemap.org/), with detail that scales
  to the size of the trip — a short run shows residential streets, a long
  tour shows only motorways and major roads
- Coastlines and lakes taken from real OpenStreetMap water polygons
- Multiple aspect ratios (portrait, A-series paper, square, landscape, story format) with layout that scales proportionally
- Adjustable map padding, to place the route in as much geographic context as you want
- Metric or imperial units
- Monochrome ink, or a colour per day for multi-day trips
- Paused recordings (ferries, transfers) are drawn as a dashed connector and
  excluded from the distance totals
- Export as SVG (editable, best for printing) or PNG

## Why

Built to make a keepsake poster of a multi-day cycling trip, then
generalized once it was clear the same approach works for any GPS
track. Everything runs client-side — your GPX data never leaves your
browser. The only network requests are for map and terrain tiles.

## Notes

Terrain and map tiles are fetched at render time, so a network connection
is needed for the hillshade and roads. Everything else — parsing, the
route, the elevation profile, export — works offline.

Some browsers block those requests when the file is opened directly from
disk (`file://`). If the terrain or roads don't load locally, serve the
folder over HTTP instead:

```
python3 -m http.server 8000
```

then open <http://localhost:8000>.

## Credits

Elevation data: Mapzen Terrain Tiles via AWS Open Data (3DEP, SRTM, GMTED).

Map data © OpenStreetMap contributors, served via OpenMapTiles / OpenFreeMap.

Bundles [pbf](https://github.com/mapbox/pbf) (BSD-3-Clause), inlined.

## License

MIT — see [LICENSE](LICENSE).
