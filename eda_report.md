# Exploratory Data Analysis: E-Commerce Sales
**Date**: 2025-05-04
**Author**: Junior Data Scientist, DataPulse Analytics

## Introduction
This report presents an exploratory data analysis of an e-commerce sales dataset, covering transactions from December 2010 to December 2011. The dataset includes details on invoices, products, quantities, prices, customers, and countries. The goal is to uncover sales trends, identify key markets, and provide actionable recommendations.

## Data Cleaning
- Loaded dataset with 541,909 rows and 8 columns.
- Dropped 135,080 rows with missing `CustomerID` and 1,454 rows with missing `Description`.
- Filtered out 9,945 rows with non-positive `Quantity` or `UnitPrice` (returns or errors).
- Converted `InvoiceDate` to datetime for time-based analysis.
- Added `TotalPrice` column (`Quantity * UnitPrice`).
- Final dataset: 397,884 rows.

## Key Findings
- **Total Sales Revenue**: $8,911,407.90
- **Average Order Value**: $22.40
- **Unique Customers**: 4,338
- **Top Country**: United Kingdom ($7,308,391.55, 82.0% of total sales)
- **Top Products by Revenue**:
  - PAPER CRAFT , LITTLE BIRDIE: $168,469.60
  - REGENCY CAKESTAND 3 TIER: $142,592.95
  - WHITE HANGING HEART T-LIGHT HOLDER: $100,448.15
  - JUMBO BAG RED RETROSPOT: $85,220.78
  - MEDIUM CERAMIC TOP STORAGE JAR: $81,416.73

## Visualizations
### Sales by Country
![Top 10 Countries by Sales](sales_by_country.png)
The UK dominates sales, followed by European countries like Germany and France.

### Sales Over Time
![Monthly Sales Trends](sales_over_time.png)
Sales show seasonal peaks, particularly in November 2011, likely due to holiday shopping.

### Order Value Distribution
![Order Value Distribution](order_value_distribution.png)
Most orders are small, with a right-skewed distribution and a few high-value outliers.

## Recommendations
- **Target UK Market**: As the UK accounts for the majority of sales, invest in loyalty programs and targeted promotions for UK customers.
- **Seasonal Campaigns**: Launch holiday promotions in Q4 (October–December) to capitalize on peak sales periods.
- **Focus on Top Products**: Prioritize inventory and marketing for high-revenue products (e.g., PAPER CRAFT , LITTLE BIRDIE).
- **Expand in Europe**: Increase marketing efforts in Germany and France, which show strong sales potential.
- **Customer Retention**: Analyze repeat purchase behavior to develop strategies for retaining high-value customers.

## Conclusion
The EDA reveals significant sales concentration in the UK, strong seasonal trends, and a few high-revenue products driving performance. By focusing on key markets, optimizing inventory, and leveraging seasonal opportunities, DataPulse Analytics can enhance revenue and customer engagement. Next steps include deeper customer segmentation and predictive modeling.
