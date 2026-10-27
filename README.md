# SoFlo Guide

SoFlo Guide is a map-first public guide to local government in Miami-Dade and Broward counties.

## Coverage

- Miami-Dade County and Broward County
- All 34 Miami-Dade municipalities and all 31 Broward municipalities
- Static pages at `/places/<slug>/` with unique titles, descriptions, canonical URLs, social previews, and GovernmentOrganization structured data
- A sitemap for search indexing

The directory is ordered by 2020 U.S. Census population count (largest first). The 2020 count is labeled on each profile so it is not mistaken for a current estimate. City hall map points are approximate community-center coordinates; the profile links to the official municipal site for current contact, address, and visiting information.

## Local preview

Open `index.html` directly or run a local static server:

```sh
python -m http.server 8000
```

No build step or API key is required. The map uses MapLibre GL JS with OpenFreeMap vector tiles. The places directory and profiles are static HTML and remain available if map assets fail to load.

## Sources and maintenance

- Official municipal websites are linked on each profile.
- Miami-Dade's official municipality directory: https://www.miamidade.gov/global/management/municipalities.page
- Broward County agencies and resident services: https://www.broward.org/AgenciesAndServices
- 2020 Census counts: https://www.census.gov/programs-surveys/decennial-census/2020-census.html

Service categories are starting points to official portals. Deep service links, office hours, and city-specific data should be checked against the municipality before they are presented as definitive. Public information changes; verify details with the responsible office.

## Deployment

This is a static Cloudflare Pages project. Each profile's `index.html` is pre-rendered under `places/<slug>/`, so city pages can be crawled and shared independently of the map.
