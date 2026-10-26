# SoFlo Guide

A map-first guide to local government in Miami-Dade and Broward counties. This first version is a usable, static prototype with searchable office markers, county filters, shareable place links, and official service links.

## Try it

Open `index.html` in a browser. For a local server, run `python -m http.server 8000` in the repository directory and visit `http://localhost:8000`.

No build step or API key is required. The map uses [Leaflet 1.9.4](https://leafletjs.com/download.html) and OpenStreetMap tiles, so the map needs an internet connection. The place list and profiles still work if map assets fail to load.

## Current coverage

This is an initial set of five featured governments, not a complete directory:

- Miami-Dade County
- Broward County
- City of Miami
- Coral Gables
- Hollywood

Office addresses and links are sourced from the respective government websites and linked in each profile. Marker coordinates are approximate. Public information can change, so visitors should verify details on official sites before traveling or submitting a request.

## Add a place

Add an object to the `places` array in `index.html`. Use a stable `id` for shareable URLs, the government office name and address, approximate marker coordinates, an official website and `source` URL for the office address, and service cards pointing to official pages. Search indexes the place and service text automatically.

## Roadmap

1. Build a verified inventory of every incorporated municipality in both counties, with canonical names and official websites.
2. Verify each City Hall or primary municipal office address and geocode its marker. Record when an office is temporarily relocated.
3. Expand each profile with structured services: permits, utilities, waste, parks, transit, public records, meetings, elected offices, and 311 or equivalent.
4. Add content review dates and a source link per service. Establish a periodic check for moved or broken government pages.
5. Add jurisdiction boundaries and address lookup so residents can distinguish a mailing city from the government that serves their home.
6. Introduce natural-language answers only after a maintained, source-backed content index exists; answers should cite the exact official page and show when it was last checked.

This site is an independent guide and is not an official government service.

