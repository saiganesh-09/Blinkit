# 🛒 Blinkit — Grocery Sales Dashboard

An interactive sales analytics dashboard built on the BlinkIT grocery dataset — **8,523 transactions across 10 outlets**, rendered entirely in the browser as a single self-contained HTML file. No backend, no build step, no dependencies to install.

### � [View Live Dashboard →](https://saiganesh-09.github.io/Blinkit/)

---

## ✨ Features

- **4 KPI cards** — Total Sales Revenue, Total Orders, Average Order Value, and Average Customer Rating, recalculated on every filter change
- **6 live filters** — Outlet Type, Location Tier, Item Category, Outlet Size, Fat Content, and Establishment Year, with a one-click reset
- **8 interactive charts** powered by Chart.js that update in real time as filters change
- **Top 5 / Bottom 5 SKU rankings** by sales revenue
- **Outlet leaderboard** — sortable performance table with sales bars and star ratings for all 10 outlets
- **Auto-computed Business Insights** — best category, best tier, and best outlet derived live from the filtered selection
- **Dark Blinkit-branded UI** — fully responsive down to mobile, zero external assets (all images embedded)

## 📊 Dashboard Sections

| Section | Visualizations |
|---|---|
| KPI Overview | Revenue, Orders, Avg Order Value, Avg Rating |
| Trends & Distribution | Sales by Establishment Year (bar) · Outlet Type share (doughnut) |
| Category & Geography | Location Tier split (doughnut) · Sales by Item Category (bar) |
| Product & Store Segmentation | Outlet Size (doughnut) · Fat Content split (doughnut) |
| Quality & Visibility | Rating Distribution (bar) · Item Visibility vs Sales (scatter) |
| Performers | Top 5 & Bottom 5 items · Outlet leaderboard table |
| Insights | Auto-generated best-performing category / tier / outlet cards |

## 🗂 Dataset

The **BlinkIT grocery sales dataset** is embedded directly in `index.html` as a JSON array — the dashboard works offline with no data fetching.

| Field | Description |
|---|---|
| `Item Identifier` | Unique SKU code (e.g. `FDX32`) |
| `Item Type` | Product category — 16 categories (Fruits & Vegetables, Snack Foods, Household, …) |
| `Item Fat Content` | `Low Fat` or `Regular` |
| `Item Visibility` | Shelf/display visibility score (0–1) |
| `Item Weight` | Item weight in kg |
| `Outlet Identifier` | Unique store code — 10 outlets (`OUT010`–`OUT049`) |
| `Outlet Establishment Year` | Store founding year (2011–2022, 9 distinct years) |
| `Outlet Size` | `Small` / `Medium` / `High` |
| `Outlet Location Type` | City classification — `Tier 1` / `Tier 2` / `Tier 3` |
| `Outlet Type` | `Grocery Store` or `Supermarket Type1/2/3` |
| `Sales` | Sales revenue (₹) |
| `Rating` | Customer rating (0–5) |

## 🔍 Key Insights

- **Tier 3 cities lead in total sales** — ₹4.72L vs ₹3.93L (Tier 2) and ₹3.36L (Tier 1), despite similar order volumes
- **Fruits & Vegetables and Snack Foods** are the top-grossing categories
- **Supermarket Type1 dominates**, accounting for ~65% of all revenue
- **Medium-sized outlets** generate the most total sales; average order value stays flat (~₹140) across all store sizes

## 🛠 Tech Stack

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Chart.js](https://img.shields.io/badge/Chart.js-4.4.1-FF6384?logo=chartdotjs&logoColor=white)

- Vanilla **HTML / CSS / JavaScript** — no frameworks
- **Chart.js 4.4.1** (CDN) for all visualizations
- Google Fonts — *Syne* (headings) + *DM Sans* (body)

## � Run Locally

No setup required — just open the file:

```bash
git clone https://github.com/saiganesh-09/Blinkit.git
cd Blinkit
start index.html   # Windows
# open index.html  # macOS
```

Or serve it with any static server (`npx serve`, VS Code Live Server, etc.). An internet connection is only needed for the Chart.js CDN and fonts.

## 📁 Project Structure

```
Blinkit/
└── index.html   # Entire app — markup, styles, dataset & logic in one file
```

## 👤 Author

Built by [Sai Ganesh](https://github.com/saiganesh-09)
