# Lesotho Administrative Divisions / Lesotho



## Overview

| Item | Details |
|------|---------|
| District | 10 |
| Constituency | 78 |
| Coordinates | ✅ Included (all levels) |
| Formats | JSON, NDJSON, CSV |
| License | CC-BY-4.0 |
| Last Updated | 2026-09-02 |
| Website | [openadmindata.org/ls](https://openadmindata.org/ls/) |
| API | [openadmindata.org/api/ls](https://openadmindata.org/api/ls/) |
| Flag | [PNG](https://onlygames.me/flags-png/ls/) · [CDN](https://www.freeflags.org/cdn/) · [CSS](https://www.freeflags.org/css/) · [Collections](https://www.freeflags.org/collections/) |
| National Anthem | [🎵 Listen & Download Lesotho National Anthem MP3](https://onlygames.me/national-anthems/ls/) |

## Browse by District

| # | District | Constituencys | Link |
|---|----|----|------|
| 1 | Quthing | 6 | [Browse](divisions/quthing/) |
| 2 | Mohale&#39;s Hoek | 8 | [Browse](divisions/mohales-hoek/) |
| 3 | Qacha&#39;s Nek | 4 | [Browse](divisions/qachas-nek/) |
| 4 | Mafeteng | 8 | [Browse](divisions/mafeteng/) |
| 5 | Maseru | 12 | [Browse](divisions/maseru/) |
| 6 | Thaba-Tseka | 6 | [Browse](divisions/thaba-tseka/) |
| 7 | Mokhotlong | 5 | [Browse](divisions/mokhotlong/) |
| 8 | Berea | 10 | [Browse](divisions/berea/) |
| 9 | Leribe | 14 | [Browse](divisions/leribe/) |
| 10 | Butha-Buthe | 5 | [Browse](divisions/butha-buthe/) |

## Data Files

| File | Format | Description |
|------|--------|-------------|
| [all-district.json](data/all-district.json) | JSON | All 10 district records |
| [all-constituency.json](data/all-constituency.json) | JSON | All 78 constituency records |
| [all-flat.json](data/all-flat.json) | JSON | Levels 1-1 flat array |
| [all-flat.ndjson](data/all-flat.ndjson) | NDJSON | Streaming format |
| [all-flat.csv](data/all-flat.csv) | CSV | Spreadsheet format |
| [hierarchy.json](data/hierarchy.json) | JSON | Nested tree |
| [schema.json](data/schema.json) | JSON Schema | Data schema |

## Quick Start

### Python

```python
import json

with open("data/all-district.json", "r", encoding="utf-8") as f:
    data = json.load(f)

for r in data:
    print(f"{r['name']['local']} ({r['name']['en']}) — {r['children_count']['constituency']} constituencys")
```

### JavaScript

```javascript
import { readFileSync } from "fs";

const data = JSON.parse(readFileSync("data/all-district.json", "utf-8"));
console.log(`Total: ${data.length} districts`);
```

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `level` | integer | 1=district, 2=constituency |
| `level_name` | object | Level label (local + English) |
| `name.local` | string | Name in local script |
| `name.en` | string | English name |
| `name.slug` | string | URL-safe slug |
| `parent` | object/null | Parent division reference |
| `ancestors` | array | Full ancestor chain |
| `children_count` | object | Count of children per level |
| `zip_codes` | array | Postal codes (where available) |
| `geo.lat` | string | Latitude (WGS84) |
| `geo.lon` | string | Longitude (WGS84) |

Full schema: [data/schema.json](data/schema.json)

## Hierarchy Browse

```
divisions/{district-slug}/
```

Constituencys are listed inline in each district's README.

## AI Integration

- [llms.txt](docs/llms.txt) — Quick reference for AI agents
- [llms-full.txt](docs/llms-full.txt) — Summary with per-district links
- [Per-district data](docs/llms-full/) — Full data by district

## Citation

```
Lesotho Administrative Divisions Dataset (CC-BY-4.0)
URL: https://github.com/open-admin-data/lesotho-administrative-divisions
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

## License

- **Data**: [CC-BY-4.0](LICENSE)

## Related

- [Open Admin Data](https://openadmindata.org) — Browse, search and explore administrative divisions for every country
- [open-admin-data](https://github.com/open-admin-data) — GitHub organization with all country repos
- [ListBase](https://www.listbase.org) — Structured reference data for every country
- [FreeFlags.org](https://www.freeflags.org) — Free flag images for every country
- [Flag CDN](https://www.freeflags.org/cdn/) — Hotlink flag images directly
- [Flag CSS](https://www.freeflags.org/css/) — CSS flag sprites for web projects
- [Flag Collections](https://www.freeflags.org/collections/) — Curated flag image packs
