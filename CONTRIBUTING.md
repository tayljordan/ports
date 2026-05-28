# Contributing

Contributions are welcome. This dataset is only as good as the data it contains — corrections, additions, and improvements are appreciated.

## What to Contribute

- **Corrections** — incorrect coordinates, country names, depth values, or other field errors
- **Missing ports** — ports or points of interest not currently in the dataset
- **Documentation** — improvements to the README, field descriptions, or usage examples

## How to Contribute

1. Fork the repository
2. Create a branch: `git checkout -b fix/port-name-correction`
3. Make your changes to `ports.json` or documentation files
4. Commit with a clear message describing what changed and why
5. Open a pull request against `main`

## Data Standards

- Coordinates must be in decimal degrees, WGS84, rounded to 2 decimal places
- Depth values must be in meters
- Country names must not have a leading "the" (e.g. `"United Kingdom"` not `"the United Kingdom"`)
- `point_of_interest` should be the common local name, not an internal code or abbreviation

## Questions

Open an issue or reach out via [LinkedIn](https://www.linkedin.com/in/tayljordan/).
