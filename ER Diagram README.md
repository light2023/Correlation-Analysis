# Comprehensive Analysis of Car Repair Shop Operations
### Introduction
Latino Garage Winnipeg North, a well-established car repair shop, has been providing vehicle services since 1971. 
To help the business maximize profitability and ensure optimal customer satisfaction, 
we have conducted a comprehensive analysis of the company's operations based on provided sales receipts (https://drive.google.com/file/)

This report details the creation of a dimensional model for sales analysis, key performance indicators (KPIs), and an analysis of the business's operational aspects.

### Part A: Dimensional Model for Sales Analysis
1. Business Requirements
The primary objective is to gain insights into various aspects of sales performance at Latino Garage Winnipeg North. The key analyses to be performed include:

- Sales by Customer: Understanding revenue contributions from individual customers.
- Sales by Vehicle: Analyzing sales data by vehicle brand, model, and year.
- Sales by Service Type: Assessing revenue from different types of services.
- Sales by Parts Used: Evaluating the sales performance of different parts.
- Sales by Shop Location: Analyzing sales across different shop locations.
- Sales Over Time: Tracking sales trends over different time periods.
### 2. Key Information from Invoice
Quantitative Data:

- Hours spent on each job: 5
- Amount charged for each job:
- Labor: $625.00
- Parts: $969.87
- Total parts and labor costs: $1,594.87
- Sales tax rate: 13%
- Total amount: $1,802.20
Qualitative Data:

- Customer details: Name, contact information
- Vehicle details: Make, model, year, color, VIN, registration number, mileage
- Job descriptions: Details of services provided
- Part details: Part number, part name
- Invoice date: September 10, 2023
- Due date: October 10, 2023
### 3. Facts and Dimensions
The sales analysis is structured around a fact table and several dimension tables:

- Fact Table (Invoice): Stores quantitative data related to each sales transaction.
- Dimension Tables:
- Customer: Contains customer details.
- Vehicle: Contains vehicle details.
- Service: Stores service types.
- Parts: Contains part details.
- Location: Stores location details.
- Date: Contains date information.
### 4. Fact Table: Invoice
The Invoice table captures the essential data needed for sales analysis. It includes:

Column Name	Description
FactSalesID	Primary Key
CustomerID	Foreign Key to Customer Table
VehicleID	Foreign Key to Vehicle Table
ServiceID	Foreign Key to Service Table
PartID	Foreign Key to Part Table
LocationID	Foreign Key to Location Table
DateID	Foreign Key to Date Table
Total_Labor_Amount	Total amount charged for labor
Total_Parts_Amount	Total amount charged for parts
Total_Amount	Total amount of the transaction
Sales_Tax	Total sales tax amount
Total_Hours	Total hours spent on the job
### 5. Dimension Tables
Each dimension table is designed to store qualitative data, which allows for more detailed analysis:

Customer:
- CustomerID (Primary Key)
- CustomerName
- CustomerAddress
- CustomerPhone
Vehicle:
- VehicleID (Primary Key)
- Make, Model, Year, Color, VIN, RegistrationNumber, Mileage
- Service:
- ServiceID (Primary Key)
- ServiceDescription
Parts:
- PartID (Primary Key)
- PartNumber, PartName, UnitPrice
Location:
- LocationID (Primary Key)
- LocationName, LocationAddress
Date:
- DateID (Primary Key)
- Date, Month, Year
### 6. ER Diagram
The following ER diagram was created using MySQL Workbench to illustrate the relationships between the tables:

![color ER sales](https://github.com/user-attachments/assets/b206d8e9-a9d2-4558-87e9-318b6a02c6fe)


### 7. Documenting the Model
The ER diagram visually represents the structure of the database, emphasizing the relationships between the fact table and dimension tables.
Each table is designed to facilitate comprehensive analysis of sales data, enabling better decision-making.

### In Summary
Invoice Table: Stores all quantitative data related to sales, linking to the relevant dimension tables for detailed analysis.
Dimension Tables: Provide the qualitative context needed to categorize and analyze sales data, enabling flexible and comprehensive reporting.
