# BlinkIT Grocery Sales Analysis

A data analysis project on BlinkIT grocery sales, done in Python. The goal is to understand how the business is performing across products, categories, outlets and locations, check that the data is reliable, find out what drives sales, and suggest practical ways to improve.

## Project background

The project is set up as a data analyst assignment at Sapphire IQ (Retail & Grocery Sales Analytics). Management wanted to know which products and outlets perform well, which ones need improvement, and what is connected with sales.

## Dataset

File: `BlinkIT Grocery Data.xlsx` (8,523 rows, 12 columns). Each row is one product sold in one outlet.

| Group | Columns |
|---|---|
| Product | Item Identifier, Item Type, Item Fat Content, Item Visibility, Item Weight |
| Outlet | Outlet Identifier, Outlet Type, Outlet Size, Outlet Location Type, Outlet Establishment Year |
| Performance | Sales, Rating |

## Tools used

Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## What the notebook covers

**Objective 1: Understand the business and its sales performance**
- Product types and categories sold
- Outlet types and locations
- Overall sales and customer ratings

**Objective 2: Make sure the data is reliable**
- Missing values (Item Weight, zero Item Visibility)
- Duplicate records
- Outliers using the IQR method
- Fixing inconsistent labels (Item Fat Content, Outlet Size)

**Objective 3: Find out what drives sales**
- Sales by product category and by outlet type, location and size
- Correlation of visibility, weight, rating and establishment year with sales
- Comparison of top and bottom performing products and outlets

**Objective 4: Help management decide**
- Pareto (ABC) analysis of categories
- Best outlets and locations
- Areas that can be improved
- Practical recommendations

## Key findings

- Total sales are about 1.20 million, and the average sale is about 141.
- Six categories (Fruits and Vegetables, Snack Foods, Household, Frozen Foods, Dairy, Canned) make up about 67% of sales.
- The two Grocery Stores sell about 76K per outlet, against about 131K per outlet for each supermarket type.
- Visibility, weight, rating and outlet establishment year show almost no correlation with sales.
- Products that are sold in more outlets have higher total sales (correlation 0.53).
- Grocery Stores sell the same value per sale as supermarkets but carry far fewer products. A simple estimate suggests about 109K extra sales (around 9%) if they matched the supermarket range.

## Recommendations

1. Keep the six core categories always in stock in every outlet.
2. Widen the product range in the Grocery Stores.
3. Review pricing, pack sizes and offers for Baking Goods, Health and Hygiene and Soft Drinks.
4. Test the 39 high-value products that are sold in 3 outlets or fewer in more outlets.
5. Test any shelf-visibility change before investing in it.

## Limitations

- The data has no price, cost, profit or date columns, so profitability and trends over time could not be analysed.
- The 109K figure is a simple estimate, not a forecast.
- Outlet sizes for three outlets (OUT010, OUT017, OUT045) were fixed using the most common value, and items with an `NC` prefix were treated as non-consumables. Both are assumptions.
- There are only 10 outlets, so outlet comparisons are based on small groups.

## How to run

1. Clone or download this repository.
2. Keep `BlinkIT Grocery Data.xlsx` in the same folder as the notebook.
3. Install the libraries: `pip install pandas numpy matplotlib seaborn openpyxl jupyter`
4. Open `BlinkIT_Grocery_Sales_Analysis_Imp.ipynb` in Jupyter Notebook and run the cells from top to bottom.

## Repository files

- `BlinkIT_Grocery_Sales_Analysis_Imp.ipynb`: the full analysis with explanations
- `BlinkIT Grocery Data.xlsx`: the dataset
- `Sapphire IQ Blinkit Grocery Sales Analysis.pdf`: the project brief
- `README.md`: this file
