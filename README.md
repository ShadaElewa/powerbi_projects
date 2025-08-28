# Project 2: HR Attrition Analysis Dashboard

### [⬅️ Back to Main Portfolio Page](../..)

An interactive, two-page dashboard designed for an HR Director to understand the key drivers of employee attrition and identify high-risk groups within the company.

---

### Dashboard Demo (GIF)

*This GIF demonstrates the key features: page navigation via buttons, cross-filtering, and dynamic visuals that allow for root cause analysis.*




---

### Page 1: Attrition Overview

*This page provides a high-level executive summary of the overall attrition problem.*

<img width="1267" height="712" alt="Page1_Attrition Overview" src="https://github.com/user-attachments/assets/0a6f0649-6a34-467e-943b-54ac334614a2" />


### Page 2: Deep Dive Analysis

*This page allows for interactive root cause analysis, enabling the user to explore the factors that drive attrition.*

<img width="1252" height="712" alt="page2_DeepDiveAnalysis" src="https://github.com/user-attachments/assets/67e86c77-baae-42b2-a7ce-cdc607ff3ff2" />


---

### 1. The Business Request (Scenario)

The objective was to create a BI solution for an HR department concerned about rising employee turnover. The goal was to move beyond simple counts and build an analytical tool that could answer "Why are people leaving?" and "Who is most at risk?".

---

### 2. Technical Process & Skills Demonstrated

*   **Data Modeling:** Transformed a single flat CSV file into a robust **Star Schema Data Model**. I created dedicated dimension tables (`dimDemographics`, `dimJobDetails`, `dimSurveyResults`) to improve performance and enable more complex analysis.
*   **Data Transformation (Power Query):** Performed extensive data cleaning and feature engineering. A key step was creating new calculated columns for `Age Group` and `Salary Band` using conditional logic to turn continuous data into usable categories for analysis.
*   **Advanced DAX:** Wrote over 10 DAX measures, moving beyond simple aggregations. The core of the analysis was powered by the **`CALCULATE`** function to create sophisticated measures like `Attrition Rate` and to analyze metrics for specific segments (e.g., `Avg Monthly Income (Leavers)`).
*   **Interactive Visualization:** Designed a two-page report with a focus on user experience (UX). Implemented **navigation buttons and bookmarks** to create a guided story. The "Deep Dive" page was designed to be fully interactive, allowing users to cross-filter visuals to discover insights for themselves.

---

### 3. Key Findings & Actionable Insights

*   **Primary Driver:** The analysis revealed that **low compensation** is the single largest driver of attrition. Employees in the lowest salary band (< $3,000) have a disproportionately high attrition rate.
*   **High-Risk Profile:** The highest-risk employees are **young (20-29), in junior-level roles (Sales Reps, Lab Techs, HR), overworked (frequently work overtime), and have not been promoted in 1-2 years.**
*   **Recommendation:** A two-pronged retention strategy is recommended: 1) A review of the compensation structure for entry-level roles. 2) The development of a clear career progression path for high-performing junior employees.

---

### 4. Tools Used

*   Power BI Desktop
*   DAX (including advanced `CALCULATE` functions)
*   Power Query (M) (for ETL and Feature Engineering)
