# Vinodex map data

Appellation maps made for Vinodex, a wine encyclopedia for iOS. This repository
holds the map data the app draws from OpenStreetMap, offered here as the Open
Database License asks.

**Contains data © OpenStreetMap contributors, available under the Open
Database License (ODbL) 1.0.** See [LICENSE](LICENSE) and
<https://www.openstreetmap.org/copyright>.

These files are offered under the ODbL 1.0. Nothing else from the app (its
code, art or wine data) is covered by this license or included here.

## What is here

Seven map sets, one folder each under `planes/`:

| plane | OpenStreetMap data used | other sources |
|---|---|---|
| `spain-galicia` | concellos and parroquias (admin_level 8 and 9) | the DO pliegos' parroquia lists |
| `croatia-slavonia` | gradovi and općine (admin_level 7) | the PDO Slavonija specification |
| `greece-crete` | communities (admin_level 9 and 10) | the PDO technical files |
| `greece-thessaly` | the municipalities of Tyrnavos and Elassona, the regional units of Magnesia and the Sporades | Copernicus DEM GLO-90 |
| `greece-macedonia` | the regional units of Drama, Kavala and Thasos | Copernicus DEM GLO-90 |
| `austria-styria` | the Mur river centerline | Statistik Austria Gemeinden (CC BY 4.0) |
| `italy-valledaosta` | the Dora Baltea river centerline | ISTAT comuni (CC BY 4.0), Copernicus DEM GLO-90 |

Each folder holds four files:

| file | what it is |
|---|---|
| `pl-<plane>.json` | the plane's appellation areas as GeoJSON polygons, with their sources |
| `<plane>-manifest.json` | the map's projection and canvas, and each area's id, fill color, size in cells and button position |
| `<plane>-index.png` | the map raster: one byte per cell naming the area drawn there |
| `<plane>-region-index.json` | each area's appellation name, and the appellations listed but not drawn, with the reason |

## Sources and credits

- OpenStreetMap data from the Geofabrik extracts of 26 October 2026.
  © OpenStreetMap contributors, ODbL 1.0.
- Copernicus DEM GLO-90: © DLR e.V. 2010-2014 and © Airbus Defence and Space
  GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA; all
  rights reserved.
- Statistik Austria, Gemeinden (CC BY 4.0).
- ISTAT, confini delle unità amministrative (CC BY 4.0).
- Appellation boundaries follow each appellation's official specification.

Updated whenever a release of the app changes one of these map sets.
