# Philadelphia Crash Data Explorer

An interactive web map for exploring Philadelphia crash records by selecting street segments on the map.  
As users click street centerline segments, the app highlights selected streets, filters crashes near those streets, and summarizes crash outcomes in a sidebar table.

## What This App Does

- Displays Philadelphia street centerline segments in Mapbox GL
- Lets users click streets to select/unselect segments
- Builds a selected segment set by `SEG_ID`
- Retrieves crash points within the current map extent
- Filters crashes near selected street segments
- Shows yearly crash summary metrics in a table:
  - crash count
  - people involved
  - fatalities
  - major / moderate / minor injuries

## Tech Stack

- [Vue 3](https://vuejs.org/)
- [Vite](https://vite.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js/)
- [Turf.js](https://turfjs.org/) for spatial processing
- [BootstrapVue Next](https://bootstrap-vue-next.github.io/bootstrap-vue-next/)

## Data Sources

- Philadelphia street centerline data via ArcGIS Feature Service
- Philadelphia crash data via Carto SQL API

## Project Structure

- `src/App.vue` — app shell, layout, parent state
- `src/components/Map.vue` — map initialization, click/select behavior, crash filtering logic
- `src/components/Sidebar.vue` — crash summary table UI
- `src/main.ts` — app bootstrap and plugin registration

## Getting Started

https://www.akshaymalik.com/philadelphia-crash-reporter/
