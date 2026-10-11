# AdventureWorks Sales Performance Dashboard

Interactive Power BI report built on Microsoft's AdventureWorks sample dataset
(25.2K orders, 17.4K customers, $24.9M revenue, 2020 to 2022).

## Pages
- **Exec Dashboard:** headline KPIs (revenue, profit, orders, return rate), revenue trend, orders by category, top 10 products with return rates, month-over-month cards
- **Map:** sales by country with region slicers
- **Product Detail:** actuals vs targets, price adjustment what-if, metric selector
- **Customer Detail:** customer segmentation by income level and occupation, top customers
- **Category Tooltip:** custom tooltip page (hidden)

## Data model
Two fact tables (Sales Data, Returns Data) connected to lookup tables for calendar,
customer, product, product category, product subcategory and territory.

## Key DAX measures
- Total Revenue, Total Cost, Total Profit
- Return Rate (returned quantity / sold quantity)
- Previous Month Revenue, Orders, Returns and Profit using DATEADD
- Revenue, Order and Profit Targets (previous month x 1.1) and gap measures
- YTD Revenue (DATESYTD), 10-day Rolling Revenue and 90-day Rolling Profit (DATESINPERIOD)
- Adjusted Price, Revenue and Profit driven by a what-if parameter
- Field parameters that let the user switch the metric shown across visuals

## Finding
All three Sport-100 helmet variants are in the top 10 products by orders but have
return rates of 2.7% to 3.3%, against 2.2% overall.

## Notes
- Revenue is calculated as list price x quantity, so it is a modelled figure, not transaction amounts.
- Targets are set at 10% growth on the previous month, not business-supplied.
- AdventureWorks is a Microsoft sample dataset, so findings are illustrative.

## Screenshots

## Files
`AdventureWorks.pbix`
