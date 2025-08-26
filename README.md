# Project 1: Executive Sales Dashboard

### [⬅️ Back to Main Portfolio Page](../..)

A high-level, one-page summary of sales performance designed for executive stakeholders. This dashboard provides at-a-glance insights into key performance indicators, trends, and profitability analysis.

---

### Dashboard Screenshot

*A static view of the final dashboard design.*

![Dashboard Screenshot](https://github.com/ShadaElewa/powerbi_projects/raw/sales-dashboard/sales-dashboard/Screenshot%202025-08-24%20003858.png)

---

### Dashboard Demo (GIF)

*This GIF demonstrates the interactivity of the report, including slicer functionality and cross-filtering between visuals.*

![Dashboard Demo](./sales-dashboard/dashboard-demo.gif)

---

### 1. The Business Request (Scenario)

I took on the role of a Data Analyst tasked with creating a tool for a VP of Sales, preparing for a Quarterly Business Review. The primary need was for a "single source of truth" that could provide reliable answers to key business questions in under 60 seconds, without requiring the stakeholder to sift through spreadsheets.

The key business questions to be answered were:
*   What are our core KPIs (Sales, Profit, Profit Margin)?
*   How are our sales trending over time and are there seasonal patterns?
*   Which product categories are the most profitable?
*   Which geographic markets are our strongholds and where are the opportunities?

---

### 2. The Technical Process

#### **Data Transformation (Power Query)**
*   Connected to the raw Excel data source.
*   Performed data cleaning steps including correcting data types (e.g., Postal Code to Text), removing unnecessary columns, and checking for errors to ensure data quality.

#### **Data Modeling (Star Schema)**
*   Architected a robust **Star Schema** data model from the initial flat file. This is a best practice for scalability and performance.
*   Created dedicated dimension tables for `dimProduct`, `dimCustomer`, `dimGeography`, and a DAX-generated `dimDate` table.
*   Established one-to-many relationships between the dimension tables and the central `FactSales` table.

#### **DAX & Calculations**
*   Wrote several key DAX measures in a dedicated `_Measures` table for the organization.
*   Measures created include: `Total Sales`, `Total Profit`, `Profit Margin %`, `Total Orders`, and a time intelligence measure for `Sales YTD`.

#### **Visualization & Design**
*   Designed a clean, single-page report with a professional color theme and modern UI elements like rounded corners and shadows on visuals.
*   Utilized KPI cards for instant insights, slicers for user-driven filtering (by Year and Region), and a combination of line, bar, and treemap charts to tell a clear story.

---

### 3. Insights & Recommendations

*   **Insight 1: Seasonal Performance:** The data clearly shows a significant and consistent sales spike in the final quarter (Q4) of each year, confirming a strong holiday season impact on the business.
*   **Insight 2: Profitability Drivers:** While the "Technology" category drives the highest sales, the "APAC" market generates the most profit, with the "Oceania" region being a key contributor within that market.
*   **Recommendation:** Based on the insights, I would recommend the VP of Sales to analyze the successful sales strategies in the "APAC" market to see if they can be replicated in lower-performing markets like "Canada" or "EMEA" to boost overall profitability.

---
### 4. Tools Used

*   **Power BI Desktop** (Data Modeling & Visualization)
*   **Power Query** (ETL & Data Cleaning)
*   **DAX** (Calculations & Measures)
