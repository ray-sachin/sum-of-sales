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
2. Serve the folder over a local web server (recommended to avoid browser file:// fetch restrictions). Examples:
   - Python 3: `python -m http.server 8080`
   - Node (serve): `npx serve .`
   - VS Code Live Server: Start server in this folder.

## Usage
1. Open your server URL (e.g., `http://localhost:8080`).
2. The page loads `data.csv`, sums the `Sales` column, and displays the total as a plain number in the large “Total:” field.
3. Ensure `data.csv` is CSV-formatted. The app will:
   - Use the `Sales` column if a header row contains it (case-insensitive).
   - Otherwise, assume the second column contains sales values.
   - Ignore non-numeric symbols (like `$`, `,`, spaces) and supports negatives.

## Improvements in Round 2
- Title now explicitly set to “Sales Summary SAMPLE-SEED” as required by the brief.
- More robust CSV parsing:
  - Handles quoted fields, commas within quotes, and CRLF/Unix line endings.
  - Detects a `Sales` header (case-insensitive) or gracefully falls back to the second column.
- Resilient numeric parsing:
  - Supports currency symbols, thousand separators, whitespace, and parenthesis negatives.
  - Ignores non-numeric noise safely.
- Better UX:
  - Clear loading and error status messages.
  - Clean Bootstrap 5 layout via jsDelivr CDN.
- Deterministic output in `#total-sales` (no thousands separators) to ensure reliable automated parsing/checks.