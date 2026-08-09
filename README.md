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


## Data Cleaning & Preparation

Data quality was evaluated before conducting the analysis to improve the reliability of the results. The cleaning process focused on identifying duplicate records, invalid quantities, unusually high quantities, and missing dates.

### Duplicate Records

The original detailed sales dataset contained 514,342 records. An initial duplicate check identified 1,948 exact duplicate records, representing approximately 0.38% of the dataset.

These duplicate records were removed to prevent repeated transactions from artificially increasing sales, units sold, and profitability measures.

### Zero-Quantity Records

Six records contained a quantity of zero. Because these records did not represent actual units sold, they were removed from the analytical dataset.

### Final Clean Dataset

After removing duplicate and zero-quantity records:

- Original records: 514,342
- Records removed: 1,954
- Cleaned records: 512,388
- Remaining zero-quantity records: 0

### Missing Dates

Date completeness was also evaluated. Of the 512,388 cleaned records:

- Records with dates: 411,340
- Records without dates: 101,048
- Percentage with dates: 80.28%
- Percentage without dates: 19.72%

The records without dates represented approximately 19.61% of total revenue. Because dates could not be reliably determined for these transactions, they were retained for non-time-based analysis but excluded from analyses that required a valid transaction date.

This approach preserved useful sales information while preventing unsupported assumptions about transaction timing.


## Exploratory Data Analysis

Following the data-cleaning process, exploratory data analysis (EDA) was performed to identify patterns in sales activity, product performance, customer behavior, and transaction types.

The analysis used Python and Pandas to aggregate the cleaned transactional data and calculate key performance measures, including:

- Revenue
- Cost
- Gross profit
- Profit margin
- Units sold
- Number of transactions
- Average transaction value

The analysis was conducted across several business dimensions to identify areas of strong performance and potential opportunities for management attention.

### Analysis Areas

**Time-Based Performance:** Monthly revenue, cost, gross profit, units sold, transactions, and profit margin were analyzed to identify changes in sales performance throughout 2015.

**Product Performance:** Products were evaluated based on revenue, gross profit, units sold, transaction volume, and profit margin to identify the products contributing most significantly to overall performance.

**Customer Performance:** Customer-level metrics were calculated to identify high-value customers based on revenue, gross profit, transaction activity, and average transaction value.

**Receipt-Type Performance:** Sales were grouped by receipt prefix to compare revenue, profitability, transaction volume, and average transaction value across different transaction types.

These analyses provide the foundation for the visualizations and business findings presented in the following sections.
