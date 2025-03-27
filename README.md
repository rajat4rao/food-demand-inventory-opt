# Food Demand Analysis for Meal Delivery Service using Tableau

## Table of Contents
1.  [Overview](#overview)
2.  [Problem Statement](#problem-statement)
3.  [Dataset](#dataset)
4.  [Analysis Approach & Visualization](#analysis-approach--visualization)
5.  [Key Areas of Analysis](#key-areas-of-analysis)
6.  [Technologies Used](#technologies-used)
7.  [How to View the Analysis](#how-to-view-the-analysis)
8.  [File Structure](#file-structure)
9.  [Contributing](#contributing)
10. [License](#license)

---

## Overview

This project focuses on analyzing historical food demand data for a meal delivery company operating across multiple cities and fulfillment centers. The primary goal is to leverage Tableau to visualize demand patterns, identify key trends, and provide actionable insights for optimizing inventory management (especially for perishable raw materials procured weekly) and staffing levels at each center. The analysis aims to create a comprehensive "story" within Tableau, detailing demand variations at the fulfillment center and meal-specific levels.

---

## Problem Statement

Our client is a meal delivery company with various fulfillment centers in multiple cities. They require assistance with demand forecasting for upcoming weeks to enable better planning for raw material stock and center staffing. Key challenges include:

*   **Perishable Inventory:** Most raw materials are procured weekly and are perishable, making accurate demand prediction crucial for minimizing waste.
*   **Staffing Optimization:** Accurate demand forecasts help in efficiently staffing the fulfillment centers.

The client needs an end-to-end report in Tableau that clearly visualizes demand levels. The analysis must be granular, covering both fulfillment centers and specific meal products, to understand which areas and products are performing well and which require attention. The final output should be a compelling Tableau story highlighting center-meal combination performance and overall demand dynamics.

---

## Dataset

The analysis is based on three datasets provided by the client:

1.  **`Weekly_Demand_Data.csv`**: Contains historical weekly demand figures for specific meal-center combinations.
    *   Includes columns like `week`, `center_id`, `meal_id`, `checkout_price`, `base_price`, `emailer_for_promotion`, `homepage_featured`, and `num_orders` (target variable).
2.  **`Meal_Info.csv`**: Provides features for each meal (product).
    *   Includes columns like `meal_id`, `category`, `cuisine`.
3.  **`fulfilment_center_info.csv`**: Contains information about each fulfillment center.
    *   Includes columns like `center_id`, `city_code`, `region_code`, `center_type`, `op_area`.

These datasets are linked via `meal_id` and `center_id`.

---

## Analysis Approach & Visualization

This project utilizes **Tableau** as the primary tool for data analysis and visualization. The process involves:

1.  **Data Integration:** Connecting and joining the three CSV files within Tableau using common identifiers (`center_id`, `meal_id`).
2.  **Data Exploration:** Investigating patterns, trends, and relationships within the data using Tableau's exploratory features.
3.  **Calculated Fields:** Creating new metrics or dimensions as needed (e.g., calculating discount percentages, grouping dates, defining performance tiers).
4.  **Visualization:** Building various charts and maps to represent the data effectively:
    *   Time series plots for overall demand and center-specific trends.
    *   Bar charts comparing demand across centers, categories, or meals.
    *   Geographical maps showing demand distribution by city/region.
    *   Scatter plots or heatmaps exploring relationships (e.g., price/discount vs. demand).
5.  **Dashboard & Story Creation:** Combining visualizations into interactive dashboards and a narrative story within Tableau (`.twb` file) to address the client's specific questions.

---

## Key Areas of Analysis

The Tableau workbook (`Food Demand Forcast Analysis Project.twb`) explores several key aspects:

*   **Overall Demand Trends:** Visualizing total weekly orders over time.
*   **Center Performance:** Identifying high and low-performing fulfillment centers based on order volume.
*   **Geospatial Analysis:** Mapping demand across different cities and regions.
*   **Meal Performance:** Analyzing demand by meal category, cuisine, and individual meals.
*   **Center-Meal Interaction:** Highlighting successful or struggling combinations of specific meals at particular centers.
*   **Impact of Promotions:** Assessing the relationship between promotional activities (`emailer_for_promotion`, `homepage_featured`) and order volume (if explored in the workbook).
*   **Price Sensitivity:** Investigating how `checkout_price` and discounts relate to the number of orders (if explored in the workbook).

---

## Technologies Used

*   **Tableau Desktop:** For data connection, analysis, visualization, and dashboard creation.
*   **CSV:** Data format for the input datasets.

---

## How to View the Analysis

1.  **Ensure you have Tableau:** You need Tableau Desktop or Tableau Reader installed to open the primary analysis file. Tableau Reader is free and allows viewing and interacting with Tableau workbooks.
2.  **Open the Workbook:** Download the repository files and open the `Food Demand Forcast Analysis Project.twb` file using Tableau Desktop or Tableau Reader.
3.  **Interact:** Explore the different sheets, dashboards, and stories within the workbook to understand the demand patterns and insights derived from the data.



## License

This project is licensed under the MIT License. See the `LICENSE` file for more details (if one is present in the repository).
