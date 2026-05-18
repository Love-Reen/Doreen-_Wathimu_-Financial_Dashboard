# Doreen Wathimu — Financial Insights Dashboard

A multi-sheet Excel workbook containing raw sales data, cleaned data, pivot summaries, and a visual dashboard for analysing product, segment, country, and time-based financial performance across 2013–2014.

---

## File

`Doreen__Wathimu__Financial_Dashboard.xlsx`

---

## Workbook Structure

| Sheet | Description |
|---|---|
| **DashBoard** | Visual summary — "Financial Insights Analysis" |
| **Data** | Raw transactional sales records |
| **Cleaned_data** | Processed version of the raw data with corrections applied |
| **Sales by Segment (2)** | Pivot: total sales grouped by customer segment |
| **Profit by Month (2)** | Pivot: total profit grouped by calendar month |
| **Sales by Country (2)** | Pivot: total sales grouped by country |
| **Units Sold by Product (2)** | Pivot: total units sold grouped by product |
| **Profit Margin by Segment (2)** | Pivot: profit and sales side-by-side for margin analysis |
| **Sales by Year (2)** | Pivot: total sales split by year (2013 vs 2014) |

---

## Data Schema

Both the **Data** and **Cleaned_data** sheets share this column structure:

| Column | Type | Description |
|---|---|---|
| `Segment` | Text | Customer segment (Government, Enterprise, Midmarket, Small Business, Channel Partners) |
| `Country` | Text | Sale country (Canada, France, Germany, Mexico, United States of America) |
| `Product` | Text | Product name (Amarilla, Carretera, Montana, Paseo, Velo, VTT) |
| `Discount Band` | Text | Discount tier applied (None, Low, Medium, High) |
| `Units Sold` | Number | Quantity sold in the transaction |
| `Manufacturing Price` | Currency | Cost to manufacture one unit |
| `Sale Price` | Currency | Price charged per unit |
| `Gross Sales` | Currency | Units Sold × Sale Price (before discounts) |
| `Discounts` | Currency | Total discount amount applied |
| `Sales` | Currency | Net sales revenue (Gross Sales − Discounts) |
| `COGS` | Currency | Cost of Goods Sold |
| `Profit` | Currency | Sales − COGS |
| `Date` | Date (serial) | Transaction date stored as an Excel serial number |
| `Month Number` | Integer | Numeric month (1–12) |
| `Month Name` | Text | Full month name |
| `Year` | Integer | Calendar year (2013 or 2014) |

> **Note:** The `Cleaned_data` sheet also contains extra placeholder columns (`Column3` through `Column36`) that are empty and can be ignored or removed.

---

## Key Metrics (from Pivot Sheets)

### Overall Totals
| Metric | Value |
|---|---|
| Total Net Sales | $118,745,910.26 |
| Total Profit | $16,889,039.06 |
| Total Units Sold | 1,125,168 |

### Sales by Segment
| Segment | Sales |
|---|---|
| Government | $52,504,260.67 |
| Small Business | $42,427,918.50 |
| Enterprise | $19,611,694.38 |
| Midmarket | $2,381,883.08 |
| Channel Partners | $1,820,153.64 |

### Profit by Segment
| Segment | Profit | Margin Note |
|---|---|---|
| Government | $11,388,173.17 | Highest contributor |
| Small Business | $4,143,168.50 | Second highest |
| Channel Partners | $1,312,139.94 | |
| Midmarket | $660,103.08 | |
| Enterprise | −$614,545.63 | **Loss-making segment** |

### Sales by Country
| Country | Sales |
|---|---|
| United States of America | $25,029,830.17 |
| Canada | $24,958,424.89 |
| France | $24,321,502.28 |
| Germany | $23,486,800.82 |
| Mexico | $20,949,352.11 |

### Sales by Year
| Year | Sales |
|---|---|
| 2014 | $92,330,654.75 |
| 2013 | $26,415,255.51 |

### Units Sold by Product
| Product | Units Sold |
|---|---|
| Paseo | 339,779.5 |
| VTT | 166,605 |
| Velo | 162,424.5 |
| Montana | 154,198 |
| Amarilla | 155,315 |
| Carretera | 146,846 |

### Profit by Month (Top Months)
| Month | Profit |
|---|---|
| October | $3,439,781.02 |
| December | $2,717,329.98 |
| September | $1,786,735.27 |
| November | $1,370,102.50 |
| February | $1,148,547.39 |

---

## Notable Data Quality Issues

The raw **Data** sheet contains several records with missing or blank values in fields such as `Segment`, `Country`, `Product`, `Sale Price`, `Gross Sales`, and `Year`. These have been addressed in the **Cleaned_data** sheet. Key corrections observed include:

- Imputed sale prices for records where the field was originally blank
- Removal or correction of fully empty rows
- Inconsistent casing in `Segment` (e.g., `small business` vs `Small Business`) — partially resolved in the cleaned sheet

---

## How to Use

1. **Start with the DashBoard sheet** for a high-level visual overview.
2. **Use the pivot sheets** (prefixed with the relevant dimension) for quick summaries by segment, country, product, month, or year.
3. **Reference Cleaned_data** for analysis or further modelling — it is the reliable, processed version of the raw data.
4. **Avoid the placeholder columns** (`Column3`–`Column36`) in `Cleaned_data`; they are artefacts of the data cleaning process and contain no values.

---

## Time Coverage

| Period | Date Range |
|---|---|
| Earliest record | September 2013 |
| Latest record | December 2014 |
| Primary year | 2014 (~78% of total sales) |

---

*Prepared by Doreen Wathimu*
