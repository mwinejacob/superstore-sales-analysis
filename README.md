# Superstore Sales Analysis

Analysis of customer purchase volume, monthly seasonality, category revenue and discount sensitivity, with five executive takeaways. Completed as part of the Datheon internship.

**Author:** [Jacob Tumwine]
**Tools:** Microsoft Excel (PivotTables, PivotCharts, conditional formatting)

## Dataset

The public **Superstore** sample dataset: 9,994 order lines, 793 customers and 5,009 orders from January 2015 to December 2018. This is sample data, not real company data. Total revenue is $2.30M and total profit is $286K (12.5% margin).

Data preparation: 806 extra rows (pasted "People" and "Returns" tables) were removed from the end of the file. Order and ship dates were converted from month/day/year text into real dates. Revenue is the `Sales` column, which is already net of discount. Helper columns added: Year, Month and Discount Band.

## Key takeaways

1. **Discounts above 20% destroy profit and do not increase order size.** Margin is +29.5% with no discount and +11.9% at 1-20%, then -15.3%, -40.7% and -122.6% in the higher bands. Average quantity stays at 3.7-4.0 units in every band.
2. **Sales are heavily seasonal.** September to December brings in 51.6% of revenue and November to December alone 29.5%. November is the peak (about $352K, 753 orders) and February the low (about $60K, 162 orders).
3. **Furniture sells a lot but earns almost nothing.** $742K in sales at a 2.5% margin, against 17.0% for Office Supplies and 17.4% for Technology. Tables (-8.6%) and Bookcases (-3.0%) lose money.
4. **Customers are loyal, but a fifth of them lose money.** Only 12 of 793 customers bought once. The top 20% of customers bring in 48% of revenue. 155 customers (19.5%) have negative total profit, including the largest, SM-20320.
5. **A few products earn most of the profit.** Copiers earn $55.6K at a 37.2% margin. Paper, Labels and Envelopes also earn margins above 40%.

Each takeaway has its evidence and a recommended action in the workbook and in the executive summary.

## Repository contents

| File | Description |
|---|---|
| `Superstore_Analysis.xlsx` | Excel workbook: Takeaways, Customers, Seasonality, Month x Year heatmap, Category, SubCategory and Discount sheets, plus the cleaned data |
| `Executive_Summary.pdf` | One-page summary of the findings |
| `images/` | Screenshots of the key charts |

## Method

Each analysis is a PivotTable built on the cleaned data table. Margin is profit divided by sales. Totals were checked against the source data (9,994 rows, $2,297,200.86 in sales, $286,397.02 in profit).

## Limitations

- The link between discounts and losses is a correlation. Heavy discounts may have been applied to products that were already low-margin, although the pattern appears in all three categories.
- The data covers only four years, and sales were growing over that period.
- Returns were not analysed.
