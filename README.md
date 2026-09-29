# E-commerce Sales Dashboard

An interactive Power BI dashboard for monitoring sales, gross profit, product performance, platform results, country performance, and monthly trends across a fictional global e-commerce dataset.

## Dashboard preview

![E-commerce Sales Dashboard](./E-commerce-Sales-Dashboard.pdf)

## Dashboard overview

The report provides one-page executive monitoring with:

- Total sales
- Gross profit
- Profit margin
- Units sold
- Total orders
- Global sales distribution
- Sales by product category
- Sales and profit by platform
- Monthly sales and profit trends
- Top products by sales
- Country performance table
- Year-month, country, platform, and order-status slicers

## Dataset

The Excel source contains 1,000 order rows and 19 fields for 2026, including country, category, product, quantity, item price, product cost, platform, return status, customer segment, region, discount, payment method, shipping mode, order status, rating, and sales representative.

Data-quality checks found no duplicate rows. Rating is missing for 41 records, which correspond to non-completed orders in the sample.

## KPI results

| KPI | Result |
|---|---:|
| Total sales | 1.79M |
| Gross profit | 588.35K |
| Profit margin | 32.84% |
| Units sold | 6,490 |
| Total orders | 1,000 |

The dashboard defines total sales as `Quantity × Item Price` and gross profit as `Quantity × (Item Price - Product Cost)`. The available `Discount` field is not deducted from these headline measures, so the sales KPI represents gross merchandise sales before discount.

## Key observations

- Electronics is the largest category by sales.
- Shopify has the highest platform sales, followed by eBay and Amazon.
- Headphones, laptops, smartphones, tablets, and smartwatches lead product sales.
- Country and time slicers allow users to isolate regional and monthly performance.

## Data model

The Power BI model contains:

- `Ecom_Sales_Data`: order-level fact table
- `Calender`: date table used for month-level analysis
- A relationship between order date and calendar date
- Calculated columns and measures for revenue, gross profit, margin, orders, and units

## Repository contents

```text
.
├── E-commerce.pbix
├── Ecommerce_Sales_Dataset.xlsx
├── E-commerce-Sales-Dashboard.pdf
├── dashboard-preview.png
├── ecommerce.png
└── README.md
```

## How to use

1. Download the repository.
2. Open `E-commerce.pbix` in Microsoft Power BI Desktop.
3. If the source path is unavailable, update the Excel data-source setting to `Ecommerce_Sales_Dataset.xlsx`.
4. Refresh the model.
5. Use the dropdown slicers to filter the report.

The PDF provides a static preview for users who do not have Power BI Desktop.

## Skills demonstrated

- Power Query data preparation
- DAX calculated columns and measures
- Calendar-table modeling
- KPI design
- Interactive slicers and cross-filtering
- Map, bar, combo, and table visualizations
- Executive dashboard layout and visual hierarchy

## Limitations and next steps

- The dataset is fictional and should not be used for real commercial forecasting.
- Revenue is shown before discount; add net revenue and net margin for a finance-ready view.
- Add return rate, cancellation rate, average order value, and customer-level repeat-purchase metrics.
- Add year-over-year comparison when multiple years become available.
- Confirm dataset redistribution rights before publishing the Excel source.
