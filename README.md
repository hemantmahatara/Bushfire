# Bushfire Susceptibility – Hume & Gippsland

3D WebGIS dashboard for the GEOM1163 GIS Principles project (RMIT University).
Built with MapLibre GL JS and Chart.js — plain HTML, CSS and JavaScript, no build step.

## Run locally

The page loads JSON and images, so it needs a local web server:

```
cd 05_webgis
python -m http.server 8000
```

Then open http://localhost:8000 (or use VS Code Live Server).

## Publish on GitHub Pages

1. Push the contents of this folder to a GitHub repository.
2. Settings → Pages → Deploy from branch → `main` / root.
3. The site is served at `https://<username>.github.io/<repo>/`.

## Data

`data/` is produced by `04_scripts/build_web_data.py` from the project rasters and tables.

| File | Content |
|---|---|
| `rasters/*.png` | Display layers in Web Mercator (~230 m) |
| `rasters/query_*.png` | Encoded class values used for click queries |
| `lgas.geojson` | LGA boundaries with susceptibility and fire statistics |
| `regions.geojson` | Hume and Gippsland outlines |
| `validation_points.geojson` | 3,996 burnt / unburnt validation points |
| `stats.json` | AHP weights, class areas, validation and severity results |
| `layers.json`, `datasets.json` | Legend definitions and data sources |

Basemaps © OpenStreetMap, CARTO, Esri, OpenTopoMap. Terrain: Mapzen / AWS Terrain Tiles.
Project data: DEECA, Bureau of Meteorology, Geoscience Australia, ABS.
