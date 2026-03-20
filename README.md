# xBloom — E-Commerce Dashboard 2026

A modern, lightweight analytics dashboard for e-commerce performance tracking with real-time data visualization.

## ✨ Features

- **Executive Summary** — KPIs with sparkline trends (GMV, Visitors, Page Views, Items Sold, AOV, Conversion Rate)
- **Visual Analytics** — Monthly GMV trends, category breakdown (donut chart), product & platform performance
- **Raw Data Explorer** — Sortable, filterable data table with 50-row pagination
- **Multiple Data Sources** — Load from local Excel file or sync live from OneDrive/SharePoint
- **Live Sync** — Auto-refresh from cloud storage at configurable intervals
- **Export** — Download filtered data as CSV
- **Responsive Design** — Mobile-optimized dark theme UI

## 🚀 Quick Start

1. **Visit the live dashboard:** https://nattiyapanthong-sudo.github.io/Salesdash/

2. **Upload your Excel file:**
   - Click "Upload Excel" button
   - Select your `.xlsx` file with columns: Date, Platform, GMV, Visitors, Page Views, Items Sold, AOV, CR%, Category, Product Name, Month, Year

3. **Or connect OneDrive/SharePoint:**
   - In OneDrive, right-click your file → Share → Copy link
   - Remove the `?e=xxx` from the URL and add `?download=1` at the end
   - Paste into the "Connect" field on the dashboard

## ⚙️ Configuration

Edit the `CONFIG` object in `index.html` (around line 17):

```javascript
const CONFIG = {
  localFile: 'data.xlsx',              // Host an Excel file next to index.html
  oneDriveUrl: '',                     // Or paste your OneDrive download URL
  sheetName: 'Praew hard input Shopee', // Excel sheet name
  
  col: {
    date:      'dd/mm/yyyy',
    platform:  'platform',
    gmv:       'GMV',
    visitors:  'Visitors',
    pageViews: 'Page view',
    itemSold:  'Item sold',
    aov:       'AOV',
    cr:        'CR%',
    product:   'Product Name - 1',
    category:  'Category',
    month:     'Month',
    year:      'Year',
  },
  
  refreshInterval: 60000,  // Auto-refresh every 60 seconds (0 = disabled)
};
```

## 📊 Data Format

Ensure your Excel file has these columns (case-insensitive, but order doesn't matter):

| Date | Platform | GMV | Visitors | Page Views | Items Sold | AOV | CR% | Category | Product Name | Month | Year |
|------|----------|-----|----------|-----------|-----------|-----|-----|----------|-----------|-------|------|
| 01/01/2026 | Shopee | 50000 | 1200 | 3400 | 45 | 1111 | 3.75 | Electronics | iPhone 15 | Jan | 2026 |

## 🎨 Customization

All styling uses CSS variables in `:root`. Edit the dashboard theme:

```css
:root {
  --bg: #0b0c0e;           /* Dark background */
  --green: #b8f060;         /* Accent color (GMV/success) */
  --blue: #5eb0f5;          /* Secondary accent */
  --red: #f5605e;           /* Alerts/negative */
  /* ... and more */
}
```

## 📱 Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🔧 Libraries Used

- **Chart.js** — Interactive charts (CDN)
- **XLSX** — Excel file parsing (CDN)
- **Google Fonts** — Syne, DM Sans, DM Mono

## 📝 License

MIT — Free to use and modify

---

**Questions?** Check the in-app UI or reach out on GitHub.
