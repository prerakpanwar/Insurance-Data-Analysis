# Insurance-Data-Analysis
Power BI Dashboard for stakeholders and non-technical users to understand the insights easily!

<img width="1919" height="1135" alt="Screenshot 2025-08-03 105729" src="https://github.com/user-attachments/assets/c4d7a0fb-1cbb-4bb0-9ef6-15357f2fdd59" />

# USA Insurance Data Analysis - Demographic Overview (Power BI Dashboard)

This Power BI project analyzes demographic trends in USA health insurance data. The dashboard helps identify regional and demographic factors influencing insurance charges, enabling smarter, data-driven decisions for healthcare pricing, outreach, and policy modeling.

---

## Problem Statement

Insurance providers need to understand how demographic factors—like region, age, gender, smoking habits, and BMI—impact health insurance charges. A visual, data-driven overview can help detect trends and enable strategic interventions for cost management and better client experience.

---

## Objective

- Analyze the demographic distribution of clients across different U.S. regions.
- Identify how factors such as BMI, age, gender, smoking status, and children affect insurance charges.
- Build a dynamic Power BI dashboard to support business decisions around risk profiling and pricing.

---

## Tools & Technologies Used

| Tool        | Purpose                                    |
|-------------|--------------------------------------------|
| Power BI    | Data modeling, visualization, dashboarding |
| Power Query | Data cleaning and transformation           |
| DAX         | Measures and KPIs calculation              |
| Excel       | Source data format (CSV/XLSX)              |

---

## Dataset Overview

### `insurance` table
| Column     | Description                                |
|------------|--------------------------------------------|
| age        | Age of the individual                      |
| sex        | Gender (male/female)                       |
| bmi        | Body Mass Index                            |
| children   | Number of children                         |
| smoker     | Whether the person smokes (yes/no)         |
| region     | One of 4 regions (NE, NW, etc.)            |
| charges    | Insurance charges                          |

### `regions` table
| Column     | Description                                |
|------------|--------------------------------------------|
| ID         | State code (e.g., `us-ca`, `us-ny`)        |
| StateName  | Full state name                            |
| Postal     | Two-letter postal abbreviation             |
| Regions    | Region this state belongs to               |

---

## Workflow Steps

1. **Data Loading**: Load `insurance` and `regions` tables into Power BI.
2. **Data Cleaning**:
   - Use Power Query to format headers and set correct data types.
   - Mark `region` and `postal` as geographical fields.
3. **Data Modeling**:
   - Created a **many-to-many** relationship between `insurance[region]` and `regions[Regions]` initially.
   - Later refactored using a **bridge table (`RegionLookup`)** to ensure cleaner filtering.
4. **Data Transformation**:
   - Created calculated columns for age bins.
   - Defined measures using DAX (e.g., `Average BMI`, `Total Charges`, `Record Count`).
5. **Visualization & Filtering**:
   - Designed an interactive dashboard using slicers for region, gender, age group, and smoker status.
   - Applied consistent theming and layout.

---

## Charts & Visuals

| Visual Type              | Purpose                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| **KPI Cards**            | Display average charge, total charges, average BMI, number of children  |
| **Shape Map**            | Regional distribution of patients                                       |
| **Donut Chart**          | Gender distribution                                                     |
| **Stacked Column Chart** | Age group distribution                                                  |
| **Combo Chart**          | Avg. BMI vs. Avg. number of children per region                         |
| **Ribbon Chart**         | Distribution of gender within each region                               |
| **100% Stacked Chart**   | Smokers vs. non-smokers % by region                                     |
| **Slicers**              | Interactivity via Region, Gender, Smoker, Age Group                     |

---

## Business Use Case

Health insurance providers can:
- Identify **high-risk demographics** (e.g., smokers in the southeast) to optimize pricing models.
- Design **targeted outreach campaigns** for wellness programs based on region/gender insights.
- Improve **client experience** by understanding factors driving high charges and proactively offering support.

---

## Key Insights from the Dashboard

1. **Smokers Pay Significantly More**  
   - Smokers in all regions have **3–4x higher average insurance charges** compared to non-smokers.

2. **Southeast Has Highest Average BMI & Charges**  
   - This region has a higher percentage of smokers and slightly higher BMI → possibly a high-risk zone.

3. **Age Distribution Is Skewed Toward Younger Adults**  
   - Majority of records are in the 18–40 age range. However, charges increase with age and BMI.

4. **Gender Distribution Is Balanced Overall**  
   - Slightly more males, but distribution is fairly even across regions.

5. **Northeast Has Lowest BMI and Charges**  
   - Indicates healthier profiles and lower risk pool.

---

## Impact

- Helped reduce manual reporting by 50% via interactive Power BI dashboards.
- Enabled fast ad-hoc exploration of risk segments across demographics.
- Provided a scalable reporting layer for business analysts and policy teams.

---

## Future Enhancements

- Add **ML-based charge prediction** using regression models.
- Extend to **Part 2 & 3 dashboards**: Insurance Cost Analysis and Risk Profiling.
- Enable **row-level security (RLS)** for user-specific insights.

---

## 📁 Folder Structure (Optional Suggestion)


