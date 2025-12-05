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


<img width="370" height="472" alt="Screenshot 2025-12-05 220153" src="https://github.com/user-attachments/assets/3a1ee253-ab48-4ddb-a84d-062044dfa9be" />


## 2.2.3 Regional Performance
Regional performance is uneven, with profitability concentrated in the Northwest region at 569,398, followed by Nunavut (340,729) and the Atlantic region (225,224), while regions such as Quebec (14,422) and Yukon (6,418) are severely underpenetrated. This pattern suggests a strong foothold in select regions but also reveals untapped potential in underperforming markets. Targeted geographic expansion, price localization, or logistics restructuring could increase market penetration and reduce geographic revenue dependency.


<img width="335" height="473" alt="Screenshot 2025-12-05 220336" src="https://github.com/user-attachments/assets/f283b91e-28ee-4186-aebe-6faa18f05c2d" />

## 2.2.4 Product Category Analysis
Product category analysis shows that profitability is largely driven by Furniture, which contributes 985.36K (64.73% of total profit). Office Supplies generate 331.03K (21.74%), while Technology contributes 205.95K (13.53%). This performance imbalance is noteworthy because technology products are typically expected to deliver higher margins, signaling potential strategic misalignment in pricing, sourcing, or product mix. Sub-category analysis reinforces this point, with binders (260K), paper (242K), and furnishings (153K) performing strongly, while the copier category generates a loss of -16K. The loss is likely attributable to warranty obligations, aggressive discounting, or disproportionately high handling and delivery costs.

<img width="405" height="475" alt="Screenshot 2025-12-05 221155" src="https://github.com/user-attachments/assets/da125976-80e5-4b32-8cac-25c88f3f5047" />

## 2.2.4 Seasonal trends
Seasonal trends reveal noticeable fluctuations in monthly performance, with October (177K) and  January (174K) as the highest-earning months, and August (81K) the weakest. These fluctuations likely correlate with procurement cycles, budgeting periods, and business purchasing behaviors rather than consumer-driven trends. This presents a strategic opportunity to forecast demand cycles more precisely, align inventory availability, and deploy promotional campaigns during slower months to balance demand curves.

<img width="790" height="228" alt="Screenshot 2025-12-05 223431" src="https://github.com/user-attachments/assets/5576fd89-5c1c-4b48-8579-4a81be051f1e" />

## 3. REPORTS
## 3.1 Product Performance Analysis
Deskify’s product performance shows strong revenue contribution from certain categories, with Furniture generating the majority of total profit at 985.36K (64.73%), followed by Office Supplies at 331.03K and Technology at 205.95K. Subcategory insight reveals key performers such as binders, paper, and furnishings, while the copier category operates at a loss of -16K, suggesting pricing issues, warranty expense, or high logistics overhead. Top individual products—including Eldon ClusterMat and Panasonic models—highlight a dependency on a small set of profitable SKUs, creating product concentration risk. Operational data further indicates significant shipping cost pressure due to reliance on air freight (nearly 90% of orders), which likely diminishes margins and limits scale efficiency. Seasonal fluctuations in profitability also suggest the need for improved forecasting, inventory planning, and promotional timing. Overall, strengthening the product portfolio through cost optimization, renegotiated vendor terms, improved shipping strategy, and a focus on high-margin categories represents a key opportunity to unlock higher profitability.

<img width="1271" height="768" alt="Screenshot 2025-11-28 165734" src="https://github.com/user-attachments/assets/a76f588c-6e5d-41a4-92a2-ffcd3fa046fc" />

## 3.2 Customer performance Analysis
Customer performance analysis reveals that profitability is concentrated among a small subset of high-value buyers, such as Emily Phan (34.01K), Deborah Brumfield (31.12K), and Grant Carroll (27.98K), introducing churn vulnerability if these customers reduce or discontinue purchases. Segment-level insights show the Corporate segment contributes the highest share of profit at 527.1K, while Home Office, Consumer, and Small Business segments collectively represent a significant portion, confirming that Deskify operates in both B2B and B2C markets. Geographic performance is similarly uneven, with the Northwest region generating the highest profit at 569,398, while regions such as Yukon and Quebec remain significantly underdeveloped. These patterns signal growth opportunities through targeted marketing, regional penetration strategies, and customer loyalty initiatives. Enhancing segmentation tactics, reducing reliance on top contributors, and activating underperforming markets could diversify revenue streams and strengthen customer-driven profitability over time.

<img width="1271" height="785" alt="Screenshot 2025-11-28 165820" src="https://github.com/user-attachments/assets/77d72a84-ac2a-404d-9a7d-23a12878133e" />





