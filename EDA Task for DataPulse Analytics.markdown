# DataPulse Analytics: Junior Data Scientist Task (May 2, 2025)

## Project: Exploratory Data Analysis for E-Commerce Sales

### Objective
Perform an exploratory data analysis (EDA) on an e-commerce sales dataset to uncover insights about sales trends, customer behavior, and product performance.

### Tasks
1. **Dataset**: Obtain an e-commerce dataset (e.g., from Kaggle or UCI Repository) or use the provided structure:
   - Columns: `OrderID`, `CustomerID`, `ProductID`, `ProductCategory`, `Quantity`, `UnitPrice`, `OrderDate`, `Region`
2. **Analysis**:
   - Clean the dataset (handle missing values, outliers).
   - Compute summary statistics (e.g., total sales, average order value).
   - Identify trends (e.g., sales by time, region, or category).
   - Analyze customer patterns (e.g., repeat purchases).
3. **Visualizations**:
   - Create at least 3 plots (e.g., line plot for sales over time, bar plot for top products, histogram for order values).
   - Use matplotlib and seaborn for professional visuals.
4. **Deliverable**:
   - Python script (`eda_script.py`) with your analysis code.
   - Markdown report (`eda_report.md`) summarizing findings, including visualizations and recommendations.

### Sample Code Structure
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv('ecommerce_data.csv')

# Data cleaning
df.dropna(subset=['CustomerID', 'UnitPrice'], inplace=True)
df = df[df['Quantity'] > 0]

# Summary statistics
print(df.describe())

# Visualization 1: Sales over time
df['OrderDate'] = pd.to_datetime(df['OrderDate'])
sales_by_date = df.groupby(df['OrderDate'].dt.date)['UnitPrice'].sum()
plt.figure(figsize=(10, 6))
sales_by_date.plot()
plt.title('Total Sales Over Time')
plt.xlabel('Date')
plt.ylabel('Sales ($)')
plt.savefig('sales_over_time.png')
plt.close()

# Add more visualizations and analysis...

# Save findings to markdown
with open('eda_report.md', 'w') as f:
    f.write('# EDA Report\n')
    f.write('## Sales Trends\n')
    f.write('![Sales Over Time](sales_over_time.png)\n')
    f.write('## Key Findings\n')
    f.write('- Total sales show seasonal peaks...\n')
```

### Submission
- Submit your `eda_script.py` and `eda_report.md` in your next interaction.
- Include any questions or challenges faced for mentor feedback.

### Tips
- Ensure code is well-commented and visualizations are clear.
- Focus on actionable insights for the client (e.g., “Electronics sell best in Q4”).
- Test your script before submission to avoid errors.