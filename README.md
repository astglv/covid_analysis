# SQL Data Exploration Project: Global COVID-19 Analysis

***

## Project Summary

This project focused on **exploratory data analysis (EDA)** of global COVID-19 data using **SQL**. The primary goal was to join the separate Deaths and Vaccinations datasets and calculate key epidemiological and public health metrics, such as infection rates, mortality rates, and vaccination progress, across different countries and time periods.

---

## Datasets

The analysis was performed by integrating two key datasets:

1.  **`CovidDeaths.csv`**: Contains data on reported cases, total deaths, population, and geographic details.
2.  **`CovidVaccinations.csv`**: Contains data on total vaccinations, new vaccinations, and associated population health metrics (e.g., population vs. hospital patients).
---

## Key Analytical Tasks Performed

The SQL code performs multi-step analysis, showcasing proficiency in complex joins, aggregate functions, and window functions:

### 1. Initial Exploration
* **Joining Tables:** Established a reliable **INNER JOIN** between the `CovidDeaths` and `CovidVaccinations` tables using composite keys (`Location` and `Date`) to link deaths/cases with vaccination progress.
* **Data Filtering:** Filtered out aggregate continental and high-level records to focus the analysis on individual countries.

### 2. Epidemiological Rate Calculations
* **Total Cases vs. Total Deaths (Death Percentage):** Calculated the percentage of the population that died after being infected (Case Fatality Rate) per country and date.
* **Total Cases vs. Population (Infection Rate):** Calculated the percentage of the population that was infected with COVID-19.
* **Highest Infection Rates:** Determined which countries had the highest overall infection rates relative to their population.
* **Highest Death Counts:** Identified the countries and continents with the highest total death tolls.

### 3. Vaccination Progress Analysis
* **Rolling Population Vaccination:** Used **Window Functions** (`PARTITION BY Location, ORDER BY Date`) to calculate a running total of people newly vaccinated over time in each country.
* **Percentage of Population Vaccinated:** Calculated the percentage of the population that had received at least one vaccine dose using the running vaccination total.

### 4. Advanced Views (Reusable Queries)
* **Created SQL Views** to permanently store the results of complex calculations (e.g., `PercentPopulationVaccinated`), allowing for easier, repeatable querying and future visualization.

---

## Skills Demonstrated

| Category | Skills Demonstrated |
| :--- | :--- |
| **Technical Proficiency** | **Advanced SQL** (JOINs, Aggregate Functions, **Window Functions** (`PARTITION BY`), CTEs/Temporary Tables, **SQL Views**). |
| **Data Analytics** | **Epidemiological Rate Calculation**, Time Series Analysis (Tracking metrics over time), Data Integration, Data Cleaning/Filtering. |
| **Analytical & Scientific** | **Translating scientific concepts** (Case Fatality Rate, Infection Rate) into quantitative metrics, Handling large-scale public health data. |
