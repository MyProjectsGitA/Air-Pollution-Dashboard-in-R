Project Overview

This project is structured into four components and leverages data visualization and statistical exploration techniques in R Shiny to analyze relationships between air pollution, climate change, forest coverage, and human health outcomes. The goal is to provide interactive insights into how these environmental factors interrelate across global regions, especially in large and industrially significant countries.

Data Sources
Our World in Data – https://ourworldindata.org/air-pollution

Our World in Data (Air Pollution Risk Factors for Death Analysis) – https://ourworldindata.org/air-pollution#air-pollution-is-one-of-the-world-s-leading-risk-factors-for-death

IMF Climate Data – https://climatedata.imf.org/pages/climatechange-data

Worldometers (Largest Countries by Land Area) – https://www.worldometers.info/geography/largest-countries-in-the-world/

1. Data Preparation and Cleaning

Datasets Used
Air Quality Index (AQI) values from a global air pollution dataset.
Death percentages attributable to air pollution from the Our World in Data repository.
Annual surface temperature change sourced from the IMF climate dataset.
Forest area share from a global forestry dataset.

Cleaning and Transformation Steps

Removed rows with missing (NA) values to ensure data accuracy.
Standardized inconsistent country names across datasets to enable proper merging.
Converted year columns from wide to long format using pivot_longer() for time-series analysis.
Filtered datasets to include:
The 30 largest countries by land area for general comparisons.
The G20 nations for focused analysis of major industrial economies.
Calculated country-level averages (e.g., average AQI and average forest coverage) for comparison.

2. Exploratory Analysis and Aggregation in R

Summary Statistics Computed
Average AQI values across the 30 largest countries.
Average forest coverage percentage by country.
Air pollution-related death percentages over time for G20 nations.
Surface temperature change trends aligned with mortality rates.
Merged Datasets
Combined temperature change and air pollution death rates by country and year to explore potential relationships.
Combined forest area share and AQI values to evaluate the impact of forest coverage on air pollution.

3. Interactive Dashboard in R Shiny

The R Shiny dashboard was developed using shinydashboard, ggplot2, and plotly to enable interactive exploration. It features seven visualizations organized into sidebar menu tabs.

Dashboard Visualizations

AQI Bar Chart – Displays average AQI by country for the 30 largest countries.
Death Percentage Over Time – Line chart showing air pollution mortality trends among G20 countries.
Temperature vs. Death Percentage – Scatter plot examining the relationship between surface temperature changes and pollution-related deaths.
Forest Coverage Bar Chart – Compares average forest area share across the 30 largest countries.
AQI vs. Forest Coverage Scatter Plot – Explores the relationship between forest coverage and air pollution.
Top AQI Selector – Slider-controlled visualization displaying the countries with the highest AQI values.
Top Forest Coverage Selector – Numeric input allowing users to visualize countries with the greatest forest area.

4. Key Insights and Interpretations
Countries such as India, Saudi Arabia, Pakistan, and Mauritania exhibit high AQI levels alongside relatively low forest coverage, reinforcing the relationship between deforestation and air pollution.
G20 nations have shown relatively stable pollution-related death percentages over the past 30 years despite global environmental initiatives, suggesting additional policy improvements may be needed.
Countries including Canada and Germany maintain relatively low pollution-related mortality despite moderate temperature increases, indicating that healthcare infrastructure and environmental policies also play important roles.
Scatter plot analysis reveals only a partial relationship between temperature change, air pollution, and mortality, highlighting the multifactorial nature of climate and public health outcomes.
The dashboard enables users to interactively compare environmental indicators across countries and years, supporting deeper exploratory analysis.

5. Project Files

Below is a list of files included in this project. To run the analysis script, download all files and update the file paths as needed. A PDF version of the dashboard output is also included for reference.

Environmental_Impact_Dashboard.R – Main R script used to develop the project in RStudio.
Shiny_App_Visualizations_Summary.pdf – PDF containing all dashboard visualizations and a summary of the interactive Shiny application.
Forest_and_Carbon.csv – Dataset containing forest coverage and carbon emission data.
Global_Air_Pollution_Dataset.csv – Dataset containing global air pollution indicators.
Share_Deaths_Air_Pollution.csv – Dataset containing air pollution-related mortality statistics.
Annual_Surface_Temperature_Change.csv – Dataset containing annual surface temperature changes by country.
README.pdf – PDF version of this README document.
