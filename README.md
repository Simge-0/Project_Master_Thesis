# Project_Master_Thesis
This project analyzes the relationship between extreme heat exposure and mortality using regional weather, mortality, and population datasets.

## Data Sources

- Meteorological station-level daily weather data from the Spanish Meteorological Agency (AEMET)
- Regional mortality statistics from the National Statistics Institute of Spain (INE)
- Population and demographic data from INE, used for mortality normalization
- Administrative geographic boundary data for mapping (Eurostat GISCO)

## Data Scale

The project integrates multiple data sources and produces a large panel dataset containing demographic and mortality information across regions, months, age groups, and sex categories.

The full panel contains approximately:
- ~400,000+ rows
- 165 columns (variables)

The analytical subset used for the main regression analysis covers the 2017–2019 period.

## Project Workflow

1. Collect weather data from API (~5,000+ CSV files retrieved in 6-month chunks across multiple years)
2. Clean and standardize all datasets
3. Construct panel dataset and heat indicators
4. Run fixed effects regressions and demographic subgroup analysis
5. Generate maps and visualizations

## Tools used

Python, pandas, numpy, statsmodels, matplotlib, geopandas

## Skills Demonstrated

- Panel data construction (region × time × demographic groups)
- Fixed effects regression modeling
- Feature engineering of climate exposure indicators
- Large-scale data integration from administrative sources
- API-based data collection and batch processing (~5,000+ files)
- Data cleaning and transformation at scale
- Spatial visualization and mapping

## Key Variables

The final dataset includes constructed variables such as:
- Extreme temperature indicators (e.g. 95th percentile thresholds)
- Population-based mortality rates
- Mortality outcomes disaggregated by age group and sex

## Key Findings

- Higher extreme-temperature exposure was associated with increased mortality rates in Spain
- Effects varied across age and sex groups

## Key Outputs

- Main fixed effects regression results (table)
- Age and sex subgroup regression results
- Spatial distribution of weather stations and mortality rates (map)

## Repository Structure

Project_Master_Thesis/

Data/
- cleaned_dataset_sample.csv

Outputs/

tables/
- Main_results_table.png
- Demographic_results_table.png

maps/
- Weather_stations_coverage_per_province.png
- Average_monthly_mortality_rate_by_province.png

Scripts/
- PART_1_api.py
- PART_2_weather_cleaning.py
- PART_3_mortality_cleaning.py
- PART_4_population_cleaning.py
- PART_5_demographics_merging.py
- PART_6_panel_construction.py
- PART_7_merging_all.py
- PART_8_fixed_effects_analysis.py
- PART_9_demographic_analysis.py
- PART_10_geographic_maps.py

README.md


## Data Availability

This repository contains a curated version of the thesis analysis workflow.
Only a sample cleaned dataset (`cleaned_dataset_sample.csv`) covering the 2017–2019 analysis period is included for demonstration purposes.

Due to dataset size and processing complexity, not all raw, intermediate, robustness-check, demographic-analysis, and geospatial files used in the full thesis are included in this repository. 

The repository is intended to demonstrate the core data pipeline, feature engineering, panel-data construction, fixed effects analysis, and visualization workflow used in the project.

## Reproducibility

Due to external data sources, API-based data collection, and intermediate processing steps, the full workflow is not fully reproducible end-to-end without additional setup and external credentials.
