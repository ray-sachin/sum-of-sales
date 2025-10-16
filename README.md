# Sales Summary SPA

## Overview
A single-page application that:
- Loads Bootstrap 5 from jsdelivr CDN.
- Fetches data.csv from the same directory (attachment).
- Sums the values of the Sales column.
- Sets the document title to "Sales Summary {seed}" (defaults to "SAMPLE-SEED").
- Displays the total inside the element with id "total-sales".

## Setup
1. Place `index.html` and `data.csv` in the same directory.
2. Serve the directory with any static server, for example:
   - Python: `python3 -m http.server 8080`
   - Node (serve): `npx serve .`
   - Or open `index.html` directly in a modern browser.

No build step is required.

## Usage
- Open the app in a browser. It will fetch `data.csv`, sum the Sales column, and display the total.
- Title seeding:
  - You can pass a seed via URL query, e.g. `index.html?seed=MY-SEED`.
  - If no seed is provided, it defaults to `SAMPLE-SEED`.
- Ensure `data.csv` includes a header row with a "Sales" column (case-insensitive).