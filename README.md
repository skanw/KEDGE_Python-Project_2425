# KEDGE_Python-Project_2425

# Product Segmentation Analysis

## Overview
This project aims to analyze and segment products in the **Online Retail Dataset** based on their sales volume, revenue, and daily sales trends. The goal is to group products into meaningful segments, such as **"Fast Movers"**, **"Revenue Generators"**, and others, using clustering techniques like **K-Means**.

## Dataset
The dataset used in this analysis is the **Online Retail Dataset**, which contains information on products sold, quantities, prices, and transaction dates.
Link: [UCI Repository](https://archive.ics.uci.edu/dataset/352/online+retail)

### Relevant Fields:
1. *InvoiceNo*:
Description: Unique identifier for each transaction or invoice.

Type: String

Usage: Tracks and differentiates individual sales transactions.

2. *StockCode*:
Description: Unique identifier for each product sold.

Type: String

Usage: Represents the product or item sold in the transaction. It can be used to track sales per product.

3. *Description*:
Description: Name or description of the product sold.

Type: String

Usage: Provides more details about the product, which is useful for identifying the item by name.

5. *Quantity*:
Description: The number of units sold in the transaction.

Type: Integer

Usage: Shows how many items were sold in that transaction.

7. *InvoiceDate*:
Description: Date and time when the transaction was processed.

Type: DateTime

Usage: Provides temporal information about when a sale occurred. Useful for analyzing sales over time or identifying daily trends.

9. *UnitPrice*:
Description: Price of a single unit of the product.

Type: Float

Usage: Shows how much a single unit of the product costs. Used to calculate the total revenue for each product.

11. *CustomerID*:
Description: Unique identifier for each customer.

Type: Integer

Usage: Helps identify the customer who made the purchase, useful for analyzing customer behaviors and trends.

13. *Country*:
Description: The country where the customer resides.

Type: String

Usage: Useful for geographical analysis and segmenting customers by location.

## Approach
1. **Data Cleaning**: Remove rows with missing or invalid values in key columns (`StockCode`, `Description`, `Quantity`, `UnitPrice`, `InvoiceDate`).
2. **Revenue Calculation**: Compute total revenue for each product using the formula `Revenue = Quantity × UnitPrice`.
3. **Data Aggregation**: Group the data by product (`StockCode`, `Description`) to calculate:
   - Total Quantity sold
   - Total Revenue generated
   - Number of unique days each product was sold (Daily Sales Trends)
4. **Clustering**: Use **K-Means** clustering to segment products into groups based on total quantity, revenue, and daily sales.
5. **Cluster Interpretation**: Analyze each cluster and assign meaningful labels (e.g., "Fast Movers", "Revenue Generators").

## Requirements
- Python 3.x
- pandas
- matplotlib
- scikit-learn

## Instructions to Run
1. Install dependencies:
   ```bash
   pip install pandas matplotlib scikit-learn
   ```
2. Download the **Online Retail Dataset** from [UCI Repository](https://archive.ics.uci.edu/dataset/352/online+retail).
3. Run the script to perform the analysis and generate visualizations.

## Visualizations
- **Pareto Chart**: Visualizing the top contributors to revenue.
- **Clustering Visualization**: Scatter plot to show the segmentation of products based on total quantity and revenue.

## Conclusion
This analysis segments products into meaningful groups to identify top performers and slow-moving products, which can help with inventory management, marketing strategies, and pricing decisions.

---

Let me know if you'd like to adjust any sections!
