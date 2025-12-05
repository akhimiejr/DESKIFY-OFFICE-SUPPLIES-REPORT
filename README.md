# 1. Introduction
# DESKIFY-OFFICE-SUPPLIES-REPORT
Deskify Report is a full analytical breakdown of your dataset and visuals based on the Power BI report you provided. The analysis is grouped into categories for clarity: summary metrics, product performance, customer insights, time-series behavior, shipping mode analysis, regional analysis, and data quality/business implications
# 1.1 Overview 
Deskify Office Supply Co. is a leading retailer
specializing in office supplies,
technology/computer accessories, and furniture.
With a diverse product range catering to both
individual consumers and businesses, They have
experienced significant growth over the past four
years. Deskify Office Supply Co. is dedicated to
providing high-quality office essentials,
technology accessories, and furniture with a focus
on reliability, efficiency, and customer
satisfaction. 
# 1.2 Aim and Objective
To build a data model using Deskify Office
Supply Co.’s sales and transaction reporting
by using Power BI. This solution will
centralize data sources and streamline data
cleaning. By reducing manual processes, the
project will improve reporting accuracy and
efficiency.
Finally, Build an interactive dashboards that
will enable faster, data-driven decisions. 
# 1.3 Data Description
• Order ID: Unique identifier for each order.__
• Order Date: Date when the order was placed.__
• Order Priority: Priority level of the order (e.g., high, medium, low).__
• Order Quantity: Quantity of items in the order.__
• Discount: Discount applied to the order, as a percentage or amount.__
• Ship Mode: Shipping method selected for the order (e.g., express,
regular or delivery truck).__
• Profit: Profit earned from the order after costs.__
• Unit Price: Price per unit of the item sold.__
• Shipping Cost: Cost associated with shipping the order.
• CustID: Unique identifier for each customer.__
• Customer Name: name of the customer.__
• Customer Segment: Customer category (e.g.,
consumer, corporate, Home office, small business).__
• Country: Customer's country.__
• City: Customer's city.__
• State: Customer's state or province.__
• Postal Code: Customer's postal code.__
• Region: Geographic region of the customer.__
• Product ID: Unique identifier for each product.__
• Product Category: Broad category of the product
(e.g., furniture, office supplies).__
• Product Sub-Category: More specific category
within the product category.__
• Product Name: Name of the product.
# 2. Analysis
## 2.1 Problem Statement
The organization currently depends on Excel for
compiling, analyzing, and reporting its monthly
sales and transaction data. It has become
increasingly cumbersome and time-consuming due
to the complexity of the data and the high volume of
transactions processed each month.
Reporting process involves manual data entry,
consolidation from multiple sources which
introduces errors and inconsistencies.
## 2.2 Data Modelling 
The data model represents a well-structured star schema centered on a single fact table, TransactionFact, which stores operational data such as revenue, profit, quantity, order dates, product IDs, and customer IDs. This fact table connects to multiple supporting dimension tables, including CustomerDim, ProductDim, OrderDim, LocationDim, and CalendarDim, each providing descriptive attributes for filtering, categorization, and analysis. All relationships are appropriately configured as one-to-many from dimensions to the fact table with single-direction filtering, which aligns with best practices for analytical reporting and avoids ambiguity. A separate "Calculated Measures" table is included, demonstrating strong governance by centralizing DAX calculations for maintainability. Overall, the model is clean, scalable, and optimized for Power BI reporting, though future refinements such as hierarchies, surrogate keys, and extended cost structures could further enhance analytical depth and long-term scalability.
<img width="1388" height="645" alt="Screenshot 2025-12-05 212722" src="https://github.com/user-attachments/assets/eaa7621e-8a98-431a-bdd8-c6cfcad551a8" />
## 2.2.2 Customer Profitability Analysis
Customer profitability analysis indicates a heavy reliance on a small set of high-value buyers, including Emily Phan (34.01K), Deborah Brumfield (31.12K), and Grant Carroll (27.98K). While these customers drive significant profits, the lack of diversification introduces churn risk, meaning that the departure of only a few key clients could meaningfully impact financial performance. Segment-level analysis shows Corporate customers are the highest contributors at 527.1K, yet Home Office, Consumer, and Small Business segments together represent a substantial share, demonstrating that Deskify serves both institutional and individual markets and would benefit from tailored engagement strategies across all buyer types.
<img width="711" height="477" alt="Screenshot 2025-12-05 215521" src="https://github.com/user-attachments/assets/d6ee7d11-b3f4-4981-bb92-45ae53eb90be" />


