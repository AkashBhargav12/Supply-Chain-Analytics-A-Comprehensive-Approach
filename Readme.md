# Supply Chain Analytics: A Comprehensive Approach


![Supply Chain Analytics](Assets/Images/Analytical techniques.jpg)





# Table of Contents

- [Objective](#objective)
  - [User Story](#user-story)
  - [Target Audience](#target-audience)
  - [Data Source](#data-source)
- [Stages](#stages)
- [Design](#design)
  - [DashBoard Mockups](#dashboard-mockups)
  - [Tools Used](#tools-used)
- [Development](#development)
  - [Pseudocode](#pseudocode)
  - [Data Exploration Notes](#data-exploration-notes)
- [Data Cleaning and Testing](#data-cleaning-and-testing)
  - [Transform and Test the Data](#transform-and-test-the-data)
- [Visualisation](#visualisation)
  - [Results](#results)
  - [DAX Measures](#dax-measures)
- [Analysis](#analysis)
  - [Findings](#findings)
- [Recommendations](#recommendations)
- [Action Plan](#action-plan)
- [Key Performance Indicators (KPIs) and Monitoring Methods](#key-performance-indicators-kpis-and-monitoring-methods)
- [Conclusion](#conclusion)




# Objective

The main objective of this project is to use analytical techniques to gather insights to ensure seamless flow of products from suppliers to stores. The objectvies can be outlines as follows:

1. Segment customers based on purchasing behavior and demographics to identify the most profitable segments.
2. Identify factors influencing customer spending and predict future spending patterns.
3. Optimize inventory levels to maximize profit and minimize costs while meeting customer demand.
4. Test hypotheses regarding spending behaviors among different customer groups.
5. Identify trends and seasonal patterns in customer purchasing behavior over time.
6. Improve customer retention rates by identifying factors leading to churn.

## User Story

As the Supply Chain Manager, I want to apply various analytical techniques to our customer data so that we can derive insights and support decision-making processes for improving our supply chain operations. I need probability calculations, hypothesis testing, regression modeling, and linear programming to provide actionable recommendations for our upcoming sales and operations planning meeting.

## Target Audience

1. General Manager
2. Supply Chain Manager
3. Sales Manager
4. Operations Manager
5. Procurement Manager

## Data Source

The data for this analysis has been obtained from a confidential source and mimics real-time events, names, products, and places. It has been synthesized to mask the original source.


# Stages

- Design
- Development
- Testing
- Analysis
- Reccomendations


# Design

Based on the requirements, we can create dashboards that contain the following components, enabling the stakeholders to make informed decisions about their supply chain:
1. Overview Section
2. Customer Segmentation
3. Predictive Modeling
4. Inventory Optimisation
5. Hypothesis Testing
6. Sales Trends
7. Customer Retention
8. Interactive Filters and Drill downs


## DashBoard Mockups

What should the Dashboard Look like?

Some of the data visuals that may be appropriate in answering our questions include:

1. Table
2. Bar Chart
3. Line Chart
4. Scatter Plot
5. Text Box
6. KPI Card
7. Slicers


## Tools Used

| **Tool** | **Purpose** |
| --- | --- |
| Excel | Exploring and analyzing the data |
| MySQL Server | Cleaning and testing the data |
| Power BI | Visualizing the data via interactive dashboards |
| GitHub | Hosting the project documentation |


# Development

## Pseudocode

## Pseudocode

- How can we approach the problem to create a solution from start to finish?

  1. Get the data from a reliable data source
  2. Explore the data in Excel to check for any errors that standout
  3. Load the data into SQL Server
  4. Clean the data with SQL
  5. Test the data with SQL
  6. Load the clean data into PowerBI
  7. Generate visualisations of the data in PowerBI
  8. Perform Analysis using Excel 
  9. Generate the findings based on the insights
  10. Write the documentation + commentary
  11. Publish the insights generated
 
## Data exploration notes

This is the stage where we scan the data for errors, inconcsistencies, bugs, weird and corrupted characters etc.

- The initial observations with this dataset are as follows:

  1. The dataset comprises customer demographic and transaction data, containing 21 columns and multiple records. Key columns include customer ID, year of birth, education level, marital status, income, number of children, and various spending categories.
  2. There are no immediate indications of missing values in the dataset, suggesting a complete dataset. However, a thorough check is necessary.
  3. The dataset includes detailed demographic information such as age (derived from year of birth), education level, and marital status.
  4. Various spending categories are tracked, including wines, fruits, meat products, fish products, sweet products, and gold products.
  5. Details on customer complaints and their response to campaigns are recorded, which can be useful for customer satisfaction and engagement analysis.
  6. Although not explicitly about logistics, the dataset can provide insights into inventory management by analyzing spending patterns and purchase frequencies.
  7. Outliers exist in numerical columns such as income, spending amounts, number of purchases, and recency. These outliers require further analysis to decide whether to cap, remove, or treat them in another manner.


# Data Cleaning and Testing

The aim is to refine the dataset to ensure it is structured and ready for analysis. The cleaned data should meet the following criteria and constraints:

1. Only relevant columns should be retained.
2. All data types should be appropriate for the contents of each column.
3. No column should contain null values, indicating complete data for all records.

Below is a table outlining the constraints on our cleaned dataset,

| **Tool** | **Purpose** |
| --- | --- |
| Number of Rows | 2241 |
| Number of Columns | 18 |

### Expected Schema for Clean Data

| **Column Name**      | **Data Type**   | **Description**                                      |
|----------------------|-----------------|------------------------------------------------------|
| `CustomerID`         | `INT`           | Unique identifier for the customer                   |
| `Year_Birth`         | `INT`           | Year of birth of the customer                        |
| `Education`          | `VARCHAR(50)`   | Highest education level attained by the customer     |
| `Marital_Status`     | `VARCHAR(50)`   | Marital status of the customer                       |
| `Income`             | `DECIMAL(10,2)` | Annual income of the customer                        |
| `Kidhome`            | `INT`           | Number of children in the customer's household       |
| `Dt_Customer`        | `DATETIME`      | Date when the customer was enrolled                  |
| `Recency`            | `INT`           | Number of days since the last purchase               |
| `Complain`           | `INT`           | Whether the customer has made a complaint (0 or 1)   |
| `MntWines`           | `DECIMAL(10,2)` | Amount spent on wines                                |
| `MntFruits`          | `DECIMAL(10,2)` | Amount spent on fruits                               |
| `MntMeatProducts`    | `DECIMAL(10,2)` | Amount spent on meat products                        |
| `MntFishProducts`    | `DECIMAL(10,2)` | Amount spent on fish products                        |
| `MntSweetProducts`   | `DECIMAL(10,2)` | Amount spent on sweet products                       |
| `MntGoldProds`       | `DECIMAL(10,2)` | Amount spent on gold products                        |
| `NumDealsPurchases`  | `INT`           | Number of purchases made with a discount             |
| `NumWebPurchases`    | `INT`           | Number of purchases made through the web             |
| `NumCatalogPurchases`| `INT`           | Number of purchases made using a catalog             |
| `NumStorePurchases`  | `INT`           | Number of purchases made directly in stores          |
| `NumWebVisitsMonth`  | `INT`           | Number of visits to the company’s website in the last month |
| `Response`           | `INT`           | Whether the customer responded to a campaign (0 or 1)|

