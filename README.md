# AisleHero — public data

Runtime data for the AisleHero iOS app, fetched at app launch and cached on-device.

| File | Purpose |
|------|---------|
| `catalog-us.json` | Curated Healthier-Swaps / Top-of-Aisle catalog (US region) |
| `catalog-eu.json` | Curated catalog (EU region) |
| `rules.json` | Harmful-ingredient + threshold scoring rules |
| `app-config.json` | iOS minimum-version gate |

The catalogs and `rules.json` are refreshed monthly by the AisleHero CI updater.
Public by design — all derived from Open Food Facts + USDA FoodData Central
(both open data). The updater does not touch `app-config.json`.

## Raising the minimum iOS version

Edit `ios.minVersion` in `app-config.json` to the version you want to require
(for example `"1.2.0"`) and merge. Do that only after that version is live on
the App Store. The app blocks only when the installed version is below
`minVersion` and the App Store version is at or above it, so a `minVersion`
the store does not have yet does not force anyone. Missing or invalid JSON
fails open. The monthly rules updater does not touch this file.
