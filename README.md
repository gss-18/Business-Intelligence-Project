# DataCo Supply Chain Analysis

## Project Overview
This project focuses on analyzing the DataCo Supply Chain dataset to optimize inventory management, reduce stockouts, and enhance customer satisfaction with delivery status. The primary tools used in this project are Python, SQL Server, SSIS, and Power BI.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Description](#dataset-description)
3. [Data Preparation](#data-preparation)
4. [Data Warehouse Design](#data-warehouse-design)
5. [ETL Process](#etl-process)
6. [Power BI Visualization](#power-bi-visualization)
7. [Business Implications](#business-implications)

## Introduction
DataCo Supply Chain is a leading player in the retail industry specializing in clothing, sports, and electronic supplies. With a global presence and a diverse product range, DataCo Supply Chain focuses on efficient supply chain management and inventory optimization to drive sales and customer satisfaction.

## Dataset Description
The dataset under analysis comprises key operational metrics pertaining to the supply chain management system. It includes details on transactions, customers, products, geographical data, and order statuses.

### Data Dictionary
Refer to the dataset description section in the [Project Report](./Project_Report.docx).

## Data Preparation
Data preparation involved cleaning, preprocessing, and transforming the dataset using Python. The key steps included removing irrelevant columns, renaming columns for clarity, handling null values, and applying scaling operations.

### Key Transformations
- **Normalization**: Applied Min-Max scaling to the `product_price` column.
- **Standardization**: Applied StandardScaler to the `profit_amount` column.

Refer to the detailed data preparation steps in the [Project Report](./Project_Report.docx).

## Data Warehouse Design
Designed a star schema for the data warehouse implemented in SQL Server. The schema includes the following tables:

### Fact Table
- **Orders Fact Table**

### Dimension Tables
- **Product Dimension**
- **Customer Dimension**
- **Orders Dimension**
- **Date Dimension**

Refer to the [Star Schema](./Project_Star_Schema.pdf) for more details.

## ETL Process
The ETL process was implemented using SSIS. The process includes the following stages:

1. **Truncate DW Tables**: Clears existing data from all dimensions and fact tables.
2. **Populate Dimension Tables**: Extracts and loads data into dimension tables.
3. **Populate Orders Fact Table**: Loads data into the fact table using lookups and derived columns.

### Control Flow
![SSIS Control Flow](./Project%20Screenshots/Sussessful%20SSIS.png)

### Data Flow for Customers Dimension
![Customers Dimension Data Flow](./Project%20Screenshots/Successful%20Customer%20Dimension.png)

### Data Flow for Orders Fact Table
![Orders Fact Table Data Flow](./Project%20Screenshots/Successful%20Fact%20Table.png)

## Power BI Visualization
Power BI was used to create dynamic visualizations to analyze product sales and customer behavior.

For detailed visualization, refer to the [Project Visuals](./MIS587_Project_Vizualization.pbix).


### Key Visualizations
- **Product Sales by Department Across Various Markets**: Stacked column chart showing product sales by department across different global markets.
- **Product Category Sales Volume by Department**: Horizontal stacked chart representing the sales volume of various product categories within each department.
- **Delivery Status Slicer**: Slicer for 'Delivery Status' applied across the visualizations to allow dynamic filtering of data.

## Business Implications
1. **Strategic Overstocking in Key Departments and Markets**: Develop a strategic overstocking plan to prevent stockouts during peak shopping periods.
2. **Addressing Late Deliveries in Pacific Asia**: Improve logistic operations by collaborating with reliable local carriers and setting up a local distribution hub.
3. **Consistent Restocking of High-Demand Product Categories**: Prioritize these categories in inventory restocking strategies to avoid potential stockouts.
4. **Effective Inventory Management for Stable Demand Products**: Maintain optimal inventory levels to ensure continuous availability without overstocking.

For detailed insights and analysis, refer to the [Project Report](./Project_Report.docx).

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
