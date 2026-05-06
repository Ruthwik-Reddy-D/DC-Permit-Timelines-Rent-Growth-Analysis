# DC Permit Timelines & Rent Growth Analysis

## Project Overview

This project analyzes building permit activity and rent growth patterns in Washington, DC from 2019 to 2023. The dashboard focuses on how permit processing timelines, permit volume, permit type, and rental market growth vary across DC wards.

The goal of this project is to understand whether longer permit processing timelines are associated with higher subsequent rent growth at the ward level. The project combines public permit data, housing market data, and ward-level summary analysis to create a realistic urban analytics dashboard.

## Dashboard Preview

![DC Permit Timelines and Rent Growth Analysis](DC%20Permit%20Timelines%20%26%20Rent%20Growth%20Analysis.png)

## Project Objective

The main objective of this project is to analyze the relationship between development activity and rent growth in Washington, DC.

The dashboard is designed to answer the following questions:

1. How did building permit activity change from 2019 to 2023?
2. What was the average permit processing timeline across DC wards?
3. Which wards had longer permit processing timelines?
4. Which wards showed stronger average annual rent growth?
5. What permit types made up the largest share of permit activity?
6. Is there a visible relationship between permit processing time and rent growth?
7. Which wards stand out as high-delay or high-growth areas?

## Data Sources

The datasets used in this project come from official public data sources and trusted housing market data providers.

### Building Permit Data

Building permit data was collected from Open Data DC and Data.gov. These datasets are published by the District of Columbia Department of Buildings and include construction permits and supplemental permits such as alteration, electrical, plumbing, repair, and other permit types.

Building Permits in 2019:
https://catalog.data.gov/dataset/building-permits-in-2019

Building Permits in 2020:
https://catalog.data.gov/dataset/building-permits-in-2020

Building Permits in 2021:
https://catalog.data.gov/dataset/building-permits-in-2021

Building Permits in 2022:
https://catalog.data.gov/dataset/building-permits-in-2022

Building Permits in 2023:
https://catalog.data.gov/dataset/building-permits-in-2023

### Rent Growth Data

Rent data was collected from Zillow Research housing data.

Zillow Research Housing Data:
https://www.zillow.com/research/data/

For this project, Zillow rent data can be used to estimate annual rent growth trends for Washington, DC. Rent growth can be calculated by comparing rent index values across time.

### Housing Characteristics Data

Ward-level housing context was collected from the ACS 5-Year Housing Characteristics DC Ward dataset.

ACS 5-Year Housing Characteristics DC Ward:
https://catalog.data.gov/dataset/acs-5-year-housing-characteristics-dc-ward

This dataset provides housing characteristics such as occupancy, housing units, rooms, year built, owner/renter tenure, mortgage costs, and rent costs.

### Geographic Reference Data

DC ward boundary data can be used if a ward-level map is needed in a future version.

DC Ward Boundaries:
https://catalog.data.gov/dataset/wards-from-2022

Note: The current dashboard version avoids using a map because incorrect or AI-generated map boundaries can mislead viewers. Instead, the dashboard uses ward-level charts, tables, and ranking visuals for more reliable interpretation.

## Dashboard Metrics

The dashboard includes the following key metrics:

1. Average Permit Processing Time
2. Average Annual Rent Growth
3. Longest Average Timeline Ward
4. OLS R-squared
5. Total Ward-Year Observations
6. Monthly Permit Activity
7. Average Permit Processing Time by Ward
8. Average Rent Growth by Ward
9. Permit Mix by Type
10. Ward-Level Timeline vs. Rent Growth Relationship

## Dashboard Sections

### 1. Filter Panel

The top filter section allows the dashboard to be reviewed by year, ward, permit type, and year range.

These filters make it easier to analyze permit activity and rent growth patterns from different angles.

### 2. KPI Cards

The KPI cards summarize the most important project metrics.

The dashboard highlights:

1. Average permit processing time of 78 days
2. Average annual rent growth of 4.7%
3. Ward 7 as the ward with the longest average permit timeline
4. OLS R-squared value of 0.48
5. 40 ward-year observations

These metrics provide a quick overview of the relationship between permit timelines and rent growth.

### 3. Monthly Permit Activity

The monthly permit activity chart shows how permit volume changed from January 2019 through December 2023.

This chart helps identify periods of higher and lower permit activity. It can also show whether construction and renovation activity remained stable, increased, or declined over time.

### 4. Average Permit Processing Time by Ward

The horizontal bar chart ranks DC wards by average permit processing time.

This visual makes it easy to compare which wards experienced longer average processing timelines. Ward 7 has the highest average timeline in the dashboard, followed by Ward 8 and Ward 6.

### 5. Average Rent Growth by Ward

The rent growth bar chart compares average annual rent growth across wards.

This section helps identify which wards experienced stronger rent growth during the analysis period. Ward 7 shows the strongest average rent growth in the dashboard.

### 6. Permit Timeline vs. Rent Growth

The scatter plot compares average permit processing time with average annual rent growth by ward.

Each point represents one DC ward. The trend line helps show whether wards with longer permit timelines also tend to show higher rent growth.

The dashboard shows an R-squared value of 0.48, meaning the model explains part of the variation in rent growth. This does not prove causation, but it suggests a visible relationship worth further analysis.

### 7. Ward Comparison Ranking

The ward comparison ranking visual compares timeline rank and rent growth rank.

This is useful because it shows whether the same wards are appearing high in both permit delays and rent growth. It gives a more analytical view than a simple map and avoids misleading geographic boundary issues.

### 8. Permit Mix by Type

The donut chart shows the share of permits by permit type.

This section explains what kind of permitting activity is driving the overall permit count. Example permit categories include alteration, new building, repair, mechanical, electrical, and plumbing.

### 9. Ward Summary Table

The ward summary table provides the actual values behind the visualizations.

It includes:

1. Ward
2. Average Permit Timeline in Days
3. Average Rent Growth Percentage
4. Observation Count

This table makes the dashboard more transparent because users can verify the exact numbers shown in the charts.

### 10. OLS Regression Results

The regression table summarizes the relationship between average permit processing time and average annual rent growth.

The model shown in the dashboard is:

Average Annual Rent Growth = Intercept + Average Permit Processing Time

The dashboard includes coefficient, standard error, t-statistic, p-value, R-squared, adjusted R-squared, and observation count.

## Key Insights

1. Longer permit processing timelines are associated with higher subsequent rent growth across DC wards in this dashboard.

2. Ward 7 stands out with the longest average permit processing timeline and the highest average annual rent growth.

3. Ward 8 also shows relatively high permit timeline values and rent growth.

4. The scatter plot suggests a positive relationship between permit processing time and rent growth.

5. The R-squared value of 0.48 indicates a moderate relationship, but the analysis should be treated as observational.

6. The results do not prove that permit delays cause rent growth. Rent growth can also be affected by housing demand, income levels, construction supply, transit access, neighborhood change, and broader market conditions.

## Tools Used

This project can be built using:

1. Tableau
2. Power BI
3. Python
4. Pandas
5. Excel
6. Open Data DC
7. Data.gov
8. Zillow Research Data

## Suggested Data Cleaning Steps

The following cleaning steps can be used before dashboard development:

1. Download annual building permit datasets from 2019, 2020, 2021, 2022, and 2023.
2. Combine all annual permit files into one master permit dataset.
3. Standardize column names across all permit files.
4. Convert application date and approval date fields into proper date format.
5. Create a permit processing timeline field by subtracting application date from approval date.
6. Remove records with missing or invalid application dates.
7. Remove records with missing or invalid approval dates when calculating processing time.
8. Remove records with negative or unrealistic processing time values.
9. Standardize ward values from 1 to 8.
10. Group permit records by month, year, ward, and permit type.
11. Download rent data from Zillow Research.
12. Filter rent data to Washington, DC.
13. Calculate annual rent growth percentage.
14. Aggregate rent growth by year and ward if ward-level rent mapping is available.
15. Join permit summary data and rent growth data at the ward-year level.
16. Create ward-level summary tables for dashboard use.
17. Validate all calculated fields before publishing the final dashboard.

## Suggested Calculated Fields

### Permit Processing Time

Permit Processing Time = Approval Date - Application Date

### Average Permit Processing Time

Average Permit Processing Time = Average number of days between application date and approval date

### Annual Rent Growth Percentage

Annual Rent Growth Percentage = ((Current Year Rent Index - Previous Year Rent Index) / Previous Year Rent Index) * 100

### Ward-Year Observation

Ward-Year Observation = One ward observed for one year

Example:
8 wards x 5 years = 40 ward-year observations

### Permit Activity Count

Permit Activity Count = Number of permit records issued or approved during the selected period

### Permit Type Share

Permit Type Share = Permit Type Count / Total Permit Count

## Suggested Repository Structure

```text
DC-Permit-Timelines-Rent-Growth-Analysis/
│
├── data/
│   ├── raw/
│   │   ├── building_permits_2019.csv
│   │   ├── building_permits_2020.csv
│   │   ├── building_permits_2021.csv
│   │   ├── building_permits_2022.csv
│   │   ├── building_permits_2023.csv
│   │   ├── zillow_rent_data.csv
│   │   └── acs_housing_characteristics_dc_ward.csv
│   │
│   ├── processed/
│   │   ├── cleaned_building_permits_2019_2023.csv
│   │   ├── monthly_permit_activity.csv
│   │   ├── ward_permit_timeline_summary.csv
│   │   ├── ward_rent_growth_summary.csv
│   │   └── permit_rent_growth_model_data.csv
│
├── dashboard/
│   └── dc_permit_timelines_rent_growth_dashboard.twbx
│
├── notebooks/
│   └── data_cleaning_and_analysis.ipynb
│
├── DC Permit Timelines & Rent Growth Analysis.png
│
└── README.md
