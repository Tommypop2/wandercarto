# Wandercarto

Turn GPX files from a ride, hike, run, or paddle into a minimalist,
print-ready poster — a monochrome route map, a real elevation profile,
and genuine hillshaded terrain built from open elevation data.

No install, no account, no build step. It's a single HTML file that
runs entirely in your browser.

## Try it

- **Online:** [yourname.github.io/wandercarto](#) *(enable GitHub Pages — see below)*
- **Locally:** download `wandercarto.html` and open it directly in a browser

## Features

- Drag-and-drop any number of GPX files — sorted automatically by date/time
- Real elevation profile pulled straight from your GPX data
- Hillshaded terrain from [AWS Open Data terrain tiles](https://registry.opendata.aws/terrain-tiles/) (3DEP / SRTM / GMTED, no API key, no attribution watermark)
- Multiple aspect ratios (portrait, square, landscape, story format) with layout that scales proportionally
- Metric or imperial units
- Three palettes: monochrome ink, day-by-day color, muted film
- Export as SVG (editable, best for printing) or PNG

## Why

Built to make a keepsake poster of a multi-day cycling trip, then
generalized once it was clear the same approach works for any GPS
track. Everything runs client-side — your GPX data never leaves your
browser except for the terrain tile requests.

## Credits

Elevation data: Mapzen Terrain Tiles via AWS Open Data (3DEP, SRTM, GMTED).

## License

MIT — see [LICENSE](LICENSE).
