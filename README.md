# Pharmacy Sales Analytics

## Business Problem

A pharmacy organization needs to understand how its sales performance varies across products, customers, transaction types, and time. The available transactional data contains more than 500,000 sales records, creating an opportunity to identify revenue and profitability patterns that can support better business decisions.

The objective of this analysis is to evaluate sales performance and identify the products, customers, transaction types, and periods that contribute most significantly to revenue and gross profit. The analysis also examines data-quality issues, including duplicate transactions, zero-quantity records, unusually high quantities, and missing dates, to improve the reliability of the findings.

The analysis seeks to answer five key business questions:

1. How does revenue and gross profit change over time?
2. Which products generate the most revenue?
3. Which products generate the most gross profit?
4. Which customers contribute the most revenue?
5. Which receipt types generate the greatest sales and profitability?

The findings can help management identify high-value products and customers, understand sales trends, recognize areas requiring additional data-quality controls, and make more informed decisions about sales and operational priorities.
## Dataset & Data Sources

This project uses transactional pharmacy sales data containing detailed information about sales receipts, products, customers, quantities, prices, costs, dates, and transaction characteristics.

### Detailed Sales Dataset

- Original records: 514,342
- Records after cleaning: 512,388
- Products represented: 2,232
- Unique customers: 56,050
- Receipt types: 6
- Date coverage: January 2015 through December 2015

The detailed sales dataset was used as the primary source for product, customer, transaction, revenue, cost, and profitability analysis.

### Master Sales Dataset

- Records: 127,064
- Used to provide sales-date information and support validation of receipt records.

### Dataset Matching

The two datasets were compared using receipt identifiers. Of the unique receipts in the detailed sales data:

- Matching receipts: 126,927
- Unmatched receipts: 30,750
- Match rate: 80.5%

The unmatched receipts were primarily associated with missing dates in the detailed sales dataset. This limitation was documented rather than assuming or creating dates that were not available in the source data.
