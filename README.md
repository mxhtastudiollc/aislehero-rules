# AisleHero — public data

Runtime data for the AisleHero iOS app, fetched at app launch and cached on-device.

| File | Purpose |
|------|---------|
| `catalog-us.json` | Curated Healthier-Swaps / Top-of-Aisle catalog (US region) |
| `catalog-eu.json` | Curated catalog (EU region) |
| `rules.json` | Harmful-ingredient + threshold scoring rules |

These are refreshed monthly by the AisleHero CI updater. Public by design — all
derived from Open Food Facts + USDA FoodData Central (both open data).
