# Albatros Study Tours — interactive globe

A single self-contained HTML page showing every study tour and FAM trip the
Albatros customer service team has been on since 2014, plotted on an
interactive globe. D3, the world map and all trip data are inlined, so the
file works offline (only the web fonts are fetched remotely).

## Data

All data lives in the `TEAM`, `PLACES` and `TRIPS` arrays near the bottom of
`index.html`. To add a trip, append one object to `TRIPS` and make sure the
`place` string has an entry in `PLACES` with `[longitude, latitude]`.

- Source: "Study tour overview" (sheets OLD and 2025-2026-2027)
- Roster checked against "Vagtplan kundeservice 2026" (tab Vagtplan_2026) on
  SharePoint plus the Albatros people directory. Colleagues who have left the
  company are omitted.

## Deploy

The page is served by the LOTTA server on the Mac mini:

    cp index.html ~/lotta-server/public/study-tours/index.html

It is then available on the LAN at http://eriks-mac-mini.local:8080/study-tours/
