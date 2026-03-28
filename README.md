# superstore-sales-analysis
Data cleaning analysis, and interactive dashboard for Superstore dataset
# 📊 Superstore Sales Analysis

A complete end-to-end data analysis project using Microsoft Excel and an 
interactive Power BI-style dashboard.

---

## 📌 Project Overview

| Item | Detail |
|------|--------|
| Dataset | Sample Superstore (USA retail, 2014–2017) |
| Records | 9,994 transactions |
| Tools Used | Microsoft Excel, Power Query, DAX, PowerBI |
| Skills | Data Cleaning, Pivot Tables, Dashboard Design |

---

## 🗂️ Project Structure
```
├── data/
│   ├── Sample_-_Superstore.csv    # Raw dataset
│   └── Cleaned_Dataset.xlsx       # Cleaned & formatted data
├── analysis/
│   └── Pivot_Analysis.xlsx        # pivot tables
├── dashboard/
│   └── Superstore_Dashboard.html  # Interactive dashboard
└── README.md
```

---

## 🧹 Step 1 — Data Cleaning (Excel)

### What was done:
- ✅ Reviewed all 21 column headers and identified data types
- ✅ Checked for missing values — none found (0 blanks across all columns)
- ✅ Removed duplicates — 0 found (each Row ID is unique)
- ✅ Fixed date formatting → DD/MM/YYYY using Format Cells
- ✅ Formatted Sales & Profit as currency (`#,##0.00`)
- ✅ Formatted Discount as percentage
- ✅ Converted Postal Code to text with 5-digit zero-padding (`"00000"`)
- ✅ Standardised text to Title Case using `=PROPER(A2)`
- ✅ Trimmed 16 Product Name entries using `=TRIM(A2)`
- ✅ Validated outliers — 668 high-value sales confirmed legitimate

### New columns added:
| Column | Formula | Purpose |
|--------|---------|---------|
| Order Year | `=YEAR(C2)` | Group by year |
| Order Month Name | `=TEXT(C2,"MMMM")` | Readable month |
| Profit Margin (%) | `=Profit/Sales*100` | Profitability ratio |
| Days to Ship | `=Ship Date - Order Date` | Shipping speed |

---

## 📊 Step 2 — Pivot Table Analysis (Excel)

5 pivot tables were built to answer key business questions:

| Sheet | Question Answered |
|-------|------------------|
| PT1_Category | Which category drives the most revenue? |
| PT2_Location | Which regions and states perform best? |
| PT3_Sales_Trend | When do sales peak? Monthly & yearly? |
| PT4_Segment_Ship | What are the top 10 best-selling products? |
| PT5_Yearly_Category | How does each category grow year-over-year? |

---

## 🖥️ Step 3 — Interactive Dashboard
  
Open in any browser — no installation needed.

### Features:
- 8 KPI cards (Revenue, Profit, Transactions, Margin...)
- Monthly & yearly line charts with year filter
- Sub-category horizontal bar chart
- Pie charts for Segment and Shipping Mode
- Top 10 products table with profit margin indicators
- Slicers for Year

---

## 🔑 Key Business Insights

1. **Technology** leads revenue at **$836K (36%)** with a 15.6% profit margin
2. **California** alone generates **$457K** — more than the entire South region
3. **November** is the peak month at **$352K** — Q4 accounts for ~38% of annual revenue
4. **Furniture** earns only **$18.4K profit** on $742K sales (2.5% margin) — Tables lose money
5. Revenue grew **51.4%** from 2014 to 2017, with profit up **88.6%**

---

## 🛠️ Tools & Skills Used

- **Microsoft Excel** — Data cleaning, Power Query, Pivot Tables, Charts
- **DAX Measures** — SUM, COUNT, AVERAGE, DISTINCTCOUNT, DIVIDE
- **PowerBI** — Interactive dashboard and Data visualisation library
- **GitHub** — Version control and project documentation

---

## 👤 Author

**Temitope Oyarinu**  
[LinkedIn Profile](https://www.linkedin.com/in/temitope-oyarinu/) | [GitHub](https://github.com/ctopz)
