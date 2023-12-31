# Northwind Traders Power BI Project
![](https://github.com/chikaosx/Northwind-Traders-Power-BI-Project/blob/main/Chinonso%20dashboard.jpg)
## Project Overview
This technical documentation outlines the data analysis project conducted on the Northwind Traders dataset, with the aim of gaining valuable insights into their data. The analysis focused on extracting key information, including the number of member countries, total revenue generated, total number of traders, minimum, maximum, and average shipment costs, total revenue by country, quantity of goods bought by each customer, and the average shipping time for each shipping company.

## Project Approach

### Data Cleaning
The Northwind dataset comprises seven tables: customers, categories, orders, order_details, products, shippers, and employees. Each table underwent rigorous data cleaning using Power Query to ensure that the data was pristine and ready for analysis. The following steps were taken for data cleaning:
1. Utilized the first row as a header.
2. Renamed columns as needed.
3. Filtered columns to remove empty and blank rows.
4. Adjusted data types for specific variables.

### DAX Functions
To prepare the data for analysis and create meaningful insights, custom DAX (Data Analysis Expressions) functions were employed. Two essential custom columns were created:
1. **Revenue:** Calculated using the formula: `Revenue = (([Unit price] – [Discounts]) * [Quantity Sold])`. This allowed us to compute revenue by considering the quantity sold, unit price, and discounts.
2. **Shipping Time:** Calculated using the formula: `Shipping Time = Date.Day([Shipped Date]) - Date.Day([Order Date])`. This provided insights into the average shipping time for each shipping company.

### Data Modeling
To establish relationships between the seven distinct tables, a robust data model was constructed. Tables were modeled appropriately, and relationships were established with the following attributes:
- Categories and Products: Using the Category ID attribute, establishing a many-to-one relationship with a cross-filter direction.
- Customers and Orders: Using the Customer ID attribute, establishing a one-to-many relationship with a cross-filter direction.
- Employees and Orders: Using the Employee ID attribute, establishing a one-to-many relationship with a cross-filter direction.
- Order_Details and Orders: Using the Order ID attribute, establishing a many-to-one relationship with a cross-filter direction.
- Order_Details and Products: Using the Product ID attribute, establishing a many-to-one relationship with a cross-filter direction.
- Order and Shippers: Using the Order ID attribute, establishing a many-to-one relationship with a cross-filter direction.

### Visualization
Visualizations were crucial in conveying the key insights derived from the analysis. Various visualization elements were used:
- Visual cards: Displaying total revenue, total number of customers, and the number of Northwind Traders member countries.
- Slicers: Enabling drill-down analysis using company name and product categories.
- Treemap: Visualizing total revenue generated by each country.
- Clustered bar chart: Presenting the total quantity of goods purchased by each customer.
- Stacked bar chart: Depicting the average time it takes to ship goods in the UK and USA.
- Gauge: Displaying minimum, average, and maximum freight costs.

This project followed a systematic approach of data cleaning, manipulation, modeling, and visualization to provide comprehensive insights into the Northwind Traders dataset. The resulting Power BI dashboard offers an in-depth understanding of their business data, facilitating data-driven decision-making.
