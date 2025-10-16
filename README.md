# Sales Summary App

## Overview
A single-page web app that:
- Sets the document title to “Sales Summary SAMPLE-SEED”.
- Fetches `data.csv` (attached alongside the page).
- Sums the values in its `Sales` column.
- Displays the numeric total inside the `#total-sales` element.
- Loads Bootstrap 5 from jsDelivr for styling.

## Setup
1. Place `index.html` and `data.csv` in the same directory.
2. Serve the folder over a local web server (recommended to avoid browser file:// fetch restrictions). For example:
   - Python 3: `python -m http.server 8080`
   - Node (serve): `npx serve .`
   - VS Code Live Server: Start server in this folder.

## Usage
1. Open `http://localhost:8080` (or your server URL).
2. The page will load `data.csv`, sum the `Sales` column, and display the total in the large number next to “Total:”.
3. Ensure `data.csv` is formatted as CSV with the sales values in the second column. The first row may be a header (e.g., `Product,Sales`).