# Ando Store Management Kit

Personal store-operations web app by **Ando Hutabarat**. This is an independently written starter implementation inspired by the workflow categories visible in the public Store Head Kit reference. It does not reuse that site's source code, branding, private datasets, or proprietary templates.

## Included modules

1. **BA Blind Counting** — add rows, import an Excel/CSV stock-count file, calculate stock differences, and export a CSV report.
2. **Kepatuhan Display** — import inventory, mark items displayed/not displayed, search, and monitor display compliance.
3. **Rekap Kas** — opening cash, cash top-ups, expense entries, closing balance, and CSV export.
4. **Rekap Budget** — request and actual entries, automatic totals and remaining/over-budget calculation, and CSV export.
5. **Produk Promo** — maintain promo SKU records, discount and normal-price calculations, and CSV export.
6. **New Arrival** — maintain new-arrival records, launch date, stock/status, and CSV export.
7. **Kalkulator Lembur** — indicative overtime estimate using hourly wage = monthly wage / 173 and common PP 35/2021 multipliers. Validate with HR/payroll and current rules before using for payroll.

## Run locally

Open `index.html` in a modern browser. For best results, use a local static server (for example VS Code Live Server). Excel import uses SheetJS from jsDelivr CDN, so internet access is needed for `.xlsx` files. CSV export and manual data entry work in the browser.

## Publish with GitHub Pages

1. Create a new **public** GitHub repository, for example `ando-store-management-kit`.
2. Upload `index.html`, `styles.css`, `app.js`, and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then save.
6. Wait for the Pages deployment. The site will be available at `https://YOUR-GITHUB-USERNAME.github.io/ando-store-management-kit/`.

## Data and privacy

- App data is stored in browser `localStorage` on the device/browser where it is used.
- The app does not send store records to a backend server.
- Clearing browser data, changing browser/device, or using private browsing can remove or isolate the stored data. Export reports regularly and keep backups securely.
- Do not upload employee payroll details or confidential company inventory unless you are authorized to process that data.

## Import notes

The importer attempts to recognize common column labels such as `SKU`, `SKU Code`, `SKU Name`, `Product Name`, `Bin`, `System Qty`, `Physical Qty`, and `Quantity`. Export column names vary between retail systems; check imported values and adjust them before relying on the report. For the first version, promo and new-arrival master lists are entered manually. Inventory imports to the display-compliance module.

## Important limitations

This is a usable personal MVP, not a certified accounting, inventory, or payroll system. Exports are CSV (Excel-compatible), not formatted official forms. Overtime calculation is simplified and must be reviewed against the applicable employment agreement, wage components, local rules, and current legal requirements. No official EIGER logos, datasets, or confidential internal templates are included.
