# Amazon Sales Analysis

A concise repo-level README explaining the project: analysis of Amazon sales data to find trends, top products, revenue drivers, seasonality, and insights for decision-making. Tools used: MySQL Workbench, Excel, Canva.

Table of Contents
- Project Overview
- Key Questions
- Tools Used
- Dataset
- How to Reproduce
- File Structure
- Key Findings (high level)
- Visuals and Presentation
- Future Work
- License & Contact

Project Overview
This project analyzes Amazon sales transaction data (orders, products, customers, prices, timestamps) to extract actionable insights: top-selling SKUs, monthly revenue trends, customer segmentation, returns and refunds, and promotional effectiveness.

Key Questions
- What are the top products by revenue and units sold?
- How does revenue change month-to-month and seasonally?
- Which customer segments contribute most to revenue?
- Are there clear correlations between price, discounts, and sales volume?

Tools Used
- MySQL Workbench: data storage, cleaning, SQL queries, aggregation.
- Excel: pivot tables, quick charts, additional calculations and data snapshots.
- Canva: final visual design, presentation slides and infographic creation.

Dataset
- Source: (add dataset source here if applicable)
- Typical tables: orders, order_items, products, customers, returns
- Note: Sensitive data is excluded from repository. Use provided sample data or connect to your local dataset.

How to Reproduce
1. Import dataset into MySQL (use .sql or CSV files). 2. Open MySQL Workbench and run provided SQL scripts to create schema and aggregated views. 3. Export query results to CSV and open in Excel for pivot tables and charts. 4. Use Canva to design presentation assets using exported charts and screenshots.

Example SQL (replace table names as needed):

CREATE TABLE orders (...);
SELECT product_id, SUM(quantity) AS units_sold, SUM(quantity * price) AS revenue
FROM order_items oi
JOIN orders o ON oi.order_id = o.id
WHERE o.order_date BETWEEN '2023-01-01' AND '2023-12-31'
GROUP BY product_id
ORDER BY revenue DESC
LIMIT 20;

File Structure
- data/ (raw CSVs or SQL dumps)
- sql/ (schema and analysis queries)
- outputs/ (CSV exports, charts)
- presentation/ (Canva exports, slides)
- README.md
- PROJECT_DESCRIPTION.md

Key Findings (example placeholders)
- Top 10 products accounted for X% of revenue.
- Peak sales in November–December (holiday season).
- Discounted items saw an average increase in units sold but with margin pressure.

Visuals and Presentation
Use Excel to generate charts, then refine and annotate in Canva for the final report and presentation.

Future Work
- Add automated ETL pipeline
- Add reproducible Jupyter notebooks or dashboards
- Integrate with BI tools (Tableau/PowerBI)

License & Contact
MIT License
Author: dvssai (link to https://github.com/dvssai)