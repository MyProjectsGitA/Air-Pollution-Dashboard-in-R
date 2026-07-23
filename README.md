# Environmental Impact Dashboard

## Project Overview

This project analyzes the relationships between air pollution, climate change, forest coverage, and human health using **R Shiny**. Through interactive visualizations and statistical exploration, users can examine how environmental factors influence one another across countries and over time.

The analysis focuses on:
- Air Quality Index (AQI)
- Air pollution-related mortality
- Annual surface temperature change
- Forest area coverage

Special emphasis is placed on the **30 largest countries by land area** and the **G20 nations**, allowing users to compare environmental trends among globally significant economies.

---

# Data Sources

- **Our World in Data – Air Pollution**
  - https://ourworldindata.org/air-pollution

- **Our World in Data – Air Pollution Risk Factors for Death**
  - https://ourworldindata.org/air-pollution#air-pollution-is-one-of-the-world-s-leading-risk-factors-for-death

- **IMF Climate Data**
  - https://climatedata.imf.org/pages/climatechange-data

- **Worldometers – Largest Countries by Land Area**
  - https://www.worldometers.info/geography/largest-countries-in-the-world/

---

# 1. Data Preparation and Cleaning

## Datasets Used

- Global Air Quality Index (AQI) dataset
- Air pollution mortality dataset from Our World in Data
- Annual surface temperature change dataset from the IMF
- Global forest area coverage dataset

## Data Cleaning and Transformation

The following preprocessing steps were performed before analysis:

- Removed rows containing missing (`NA`) values.
- Standardized country names across all datasets to enable accurate merging.
- Converted year columns from wide to long format using `pivot_longer()`.
- Filtered data to include:
  - The 30 largest countries by land area.
  - The G20 nations.
- Calculated country-level averages for AQI and forest coverage.
- Prepared datasets for visualization and statistical comparison.

---

# 2. Exploratory Data Analysis

Summary statistics were generated to better understand global environmental trends.

### Analyses Performed

- Average AQI values for the 30 largest countries.
- Average forest coverage by country.
- Air pollution-related death percentages over time for G20 countries.
- Surface temperature change trends.
- Country-by-country environmental comparisons.

### Dataset Integration

Multiple datasets were merged to examine relationships between environmental indicators.

- Temperature change and pollution-related mortality were merged by country and year.
- Forest coverage and AQI data were combined to explore the relationship between forestation and air quality.

---

# 3. Interactive R Shiny Dashboard

The dashboard was developed using:

- **R Shiny**
- **shinydashboard**
- **ggplot2**
- **plotly**

The application enables users to interactively explore environmental indicators through seven visualizations.

## Dashboard Visualizations

### AQI by Country
Displays the average Air Quality Index for the 30 largest countries.

### Air Pollution Death Percentage Over Time
Shows trends in pollution-related mortality across G20 nations.

### Temperature Change vs. Death Percentage
Scatter plot illustrating the relationship between annual temperature change and pollution-related deaths.

### Forest Coverage by Country
Compares average forest area share among the 30 largest countries.

### AQI vs. Forest Coverage
Scatter plot examining the relationship between forest coverage and air pollution.

### Top AQI Countries
Interactive slider allowing users to display the countries with the highest AQI values.

### Top Forest Coverage Countries
Interactive selector displaying countries with the greatest forest area.

---

# 4. Key Findings

The analysis revealed several notable patterns.

- Countries such as **India**, **Saudi Arabia**, **Pakistan**, and **Mauritania** tend to exhibit high AQI values alongside relatively low forest coverage.
- Pollution-related mortality within G20 countries has remained relatively stable over the past three decades despite increasing environmental awareness.
- Countries including **Canada** and **Germany** maintain comparatively low pollution-related mortality despite moderate temperature increases, suggesting that healthcare systems and environmental policies also contribute to improved outcomes.
- Scatter plot analysis indicates that temperature change alone does not fully explain pollution-related mortality, highlighting the complex interaction between environmental and socioeconomic factors.
- The interactive dashboard allows users to explore these relationships dynamically across countries and time periods.

---

# 5. Project Files

To reproduce the analysis, download all project files and update the file paths in the R script as needed.

| File | Description |
|------|-------------|
| **Environmental_Impact_Dashboard.R** | Main R script used to clean, analyze, and visualize the data. |
| **Shiny_App_Visualizations_Summary.pdf** | PDF containing screenshots and summaries of all dashboard visualizations. |
| **Forest_and_Carbon.csv** | Forest coverage and carbon emissions dataset. |
| **Global_Air_Pollution_Dataset.csv** | Global Air Quality Index dataset. |
| **Share_Deaths_Air_Pollution.csv** | Air pollution mortality dataset. |
| **Annual_Surface_Temperature_Change.csv** | Annual surface temperature change dataset by country. |
| **README.pdf** | PDF version of this project documentation. |

---

# Technologies Used

- R
- RStudio
- R Shiny
- shinydashboard
- ggplot2
- plotly
- dplyr
- tidyr

---

# Author

**Amirani Kvariani**

M.S. Business Administration (Business Intelligence & Data Analytics)

Brooklyn College, City University of New York
