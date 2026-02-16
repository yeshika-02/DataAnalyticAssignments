# Sales Data Cleaning and Analysis Project

## Project Overview
This project focuses on cleaning, organizing, and analyzing sales data to extract meaningful business insights.  
The analysis is performed using Python in a GitHub Codespace environment, following proper data analytics workflow standards.

The project includes data cleaning, feature engineering, exploratory data analysis, and visualization to understand sales performance and relationships between variables.


## Dataset Description
The dataset contains 1000 sales records with the following attributes:

| Column Name      | Description                    |
|------------------|--------------------------------|
| Product_ID       | Unique identifier for products |
| Sale_Date        | Date of sale                   |
| Sales_Rep        | Sales representative           |
| Region           | Sales region                   |
| Sales_Amount     | Total sales value              |
| Quantity_Sold    | Number of units sold           |
| Product_Category | Category of product            |
| Unit_Cost        | Cost price per unit            |
| Unit_Price       | Selling price per unit         |
| Customer_Type    | New or Returning customer      |
| Discount         | Discount applied on sale       |
| Payment_Method   | Mode of payment                |
| Sales_Channel    | Online or Retail               |


## Data Cleaning Steps
The following data cleaning and preparation steps were performed:

* Converted `Sale_Date` from text to datetime format
* Removed redundant column `Region_and_Sales_Rep`
* Created calculated columns:
   **Profit** = (Unit_Price − Unit_Cost) × Quantity_Sold
   **Discounted_Sales** = Sales_Amount × (1 − Discount)
* Verified logical data consistency:
  - No negative quantities
  - Discounts within valid range
  - Checked for negative profit scenarios

The cleaned dataset was saved as `cleaned_sales_data.csv`.

## Exploratory Data Analysis
The analysis focused on answering key business questions:

### 1. Regional Sales Performance
- Identified top and low-performing sales regions
- Compared total sales across regions

### 2. Product Category Performance
- Analyzed revenue contribution by product category
- Identified high and low demand categories

### 3. Discount vs Profit Relationship
- Studied how discount rates impact profit
- Observed that higher discounts do not consistently lead to higher profit

## Visualizations
The following visualizations were created and saved:

- **Bar Chart:** Total Sales by Region
- **Bar Chart:** Sales by Product Category
- **Scatter Plot:** Discount vs Profit

All charts are stored in the `charts/` directory.

## Key Insights
- The **North region** generates the highest overall sales
- **Clothing and Furniture** categories contribute the most to revenue
- Aggressive discounting does not guarantee higher profit
- Profitability depends more on pricing strategy and volume than discounts alone

## Tools and Technologies Used
- Python
- Pandas
- Matplotlib
- Jupyter Notebook
- GitHub Codespaces
