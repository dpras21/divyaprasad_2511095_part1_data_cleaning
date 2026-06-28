# Data Cleaning and Business Analysis Project

## 1. Problem Summary

The objective of this project was to clean, validate, and analyze a retail order dataset containing sales transactions. The dataset contained missing values, duplicate records, invalid discounts, and inconsistent shipping information. The goal was to improve data quality, apply business rules, generate summary reports, and extract meaningful business insights using Excel.

---

## 2. Dataset Description

The dataset contains retail order information, including:

- Order details (`order_id`, `order_date`, `ship_date`)
- Customer information (`customer_id`, `segment`, `region`)
- Product information (`category`, `sub_category`, `product_name`)
- Sales information (`sales`, `cost`, `discount`, `profit`)
- Shipping details (`ship_mode`)
- Order status information

The raw dataset consisted of transactional sales records used for data cleaning and business reporting.

---

## 3. Tools Used

- Microsoft Excel
- Pivot Tables
- Excel Functions and Formulas
- Conditional Formatting
- GitHub
- Markdown (`.md`) for documentation

---

## 4. Cleaning Steps Performed

The following data cleaning activities were performed:

1. Examined the dataset for missing values, duplicates, and inconsistencies.
2. Removed exact duplicate records from the dataset.
3. Identified duplicate order IDs containing conflicting information.
4. Filled missing `region` values with **"Unknown"**.
5. Filled missing `ship_mode` values with **"Unknown"**.
6. Replaced missing discount values with **0** when other sales fields were valid.
7. Identified negative discount values and flagged them as invalid.
8. Identified discount values exceeding the allowed range and flagged them.
9. Identified records where ship dates occurred before order dates.
10. Created additional calculated columns:
- `calculated_sales`
- `calculated_profit`
- `profit_margin`
- `order_month`
- `order_year`
11. Created a data quality flag column to classify records as clean or flagged.

---

## 5. Business Rules Applied

The following business rules were applied during the cleaning process:

- Missing `region` values were replaced with **"Unknown"** and flagged.
- Missing `ship_mode` values were replaced with **"Unknown"** and flagged.
- Missing discount values were treated as **0** only if all other sales fields were valid.
- Negative discount values were flagged as invalid.
- Discount values above the allowed business range were flagged as invalid.
- Cancelled orders were excluded from completed sales summaries.
- Failed payment orders were excluded from completed sales summaries.
- Refunded orders were summarized separately.
- Ship dates earlier than order dates were flagged as invalid shipping records.

---

## 6. Summary of Data Quality Issues Found

The following data quality issues were identified:

- Missing values in `region`
- Missing values in `ship_mode`
- Missing values in `discount`
- Exact duplicate records
- Duplicate order IDs with conflicting information
- Negative discount values
- Discounts exceeding allowed limits
- Invalid shipping dates (ship date before order date)

These issues were corrected or flagged during the cleaning process.

---

## 7. Summary of Final Pivot Reports

The following pivot reports were created:

### Sales and Profit by Region

- Summarized total sales and profit across all regions.
- Regions were sorted from highest to lowest sales.

### Sales and Profit by Category and Sub-category

- Compared product categories and sub-categories based on sales and profitability.

### Order Count by Ship Mode

- Analyzed the number of orders processed through each shipping mode.

### Profit Margin by Customer Segment

- Compared profitability across different customer segments.

### Refunded/Cancelled/Failed Orders by Region

- Analyzed problematic orders by region for operational insights.

### Monthly Sales Trend

- Evaluated sales performance trends across different months.

---

## 8. Key Business Insights

- Certain regions generated significantly higher sales and profits than others.
- Some product categories contributed more revenue but lower profitability.
- Standard shipping mode handled the highest number of orders.
- Customer segments differed considerably in profit margins.
- Cancelled, refunded, and failed orders impacted overall business performance.
- Monthly sales trends revealed fluctuations in business demand.

---

## 9. Assumptions and Limitations

### Assumptions

- Missing region values were assumed as **"Unknown"**.
- Missing ship mode values were assumed as **"Unknown"**.
- Missing discount values were considered as **0** only when other fields were valid.
- Flagged records were retained for analysis rather than being deleted.

### Limitations

- Some conflicting duplicate records require manual business verification.
- External validation of customer and product information was not performed.
- Business assumptions were applied where complete information was unavailable.

---

## 10. Screenshots Included

The repository includes the following screenshots:

- `raw_data_preview.png`
- `cleaned_data_preview.png`
- `pivot_summary_1.png`
- `pivot_summary_2.png`

These screenshots provide evidence of the raw dataset, cleaned dataset, and pivot summary reports.
