# Changelog

## [v2.0.0] — 2026-05-28

### Added
- Merged with NGA World Port Index Publication 150 (2019 edition)
- Depth soundings: channel, anchorage, cargo pier, oil terminal (min/max in meters)
- Mean tidal range (meters)
- Entrance restrictions: tide, heavy swell, ice, other natural factors
- Maximum vessel size accommodated
- Port size classification: Major, Minor, Small, Very Small
- Metadata block: schema version, coverage stats, attribution, disclaimer, coordinate datum (WGS84)
- 1,780 location-only points of interest from original dataset retained
- MIT LICENSE file

### Changed
- Total records: 3,898 → 5,410
- Top-level structure changed from array to wrapped object: `{"metadata": {...}, "ports": [...]}`
- Field renamed: `CITY` → `point_of_interest`
- Field renamed: `harbor_size` → `port_size`
- Coordinates rounded to 2 decimal places
- Country names standardized (removed leading "the")

### Breaking Changes
- Access ports via `data["ports"]`, not `data` directly

---

## [v1.0.0] — 2024

### Initial release
- 3,898 worldwide maritime ports and points of interest
- Fields: city, state, country, latitude, longitude
