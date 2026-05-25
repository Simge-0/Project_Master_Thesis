# Project_Master_Thesis
This project analyzes the relationship between extreme heat exposure and mortality using regional weather, mortality, and population datasets.

## Data Sources

- Meteorological station-level daily weather data from the national meteorological institute of Spain (AEMET)
- Regional mortality statistics from the national statistics agency of Spain (INE)
- Population and demographic data from the national statistics agency, used for mortality normalization (INE)
- Administrative geographic boundary data for mapping (Eurostat GISCO)

## Project Workflow

1. Collect weather data from API
2. Clean and standardize datasets
3. Construct panel dataset and heat indicators
4. Run fixed effects regressions and demographic subgroup analysis
5. Generate maps and visualizations

## Tools used

Python, pandas, numpy, statsmodels, matplotlib, geopandas

## Key Methods

- Fixed effects regression
- Panel data analysis
- Feature engineering
- Spatial visualization

## Key Findings

- Higher extreme-temperature exposure was associated with increased mortality rates in Spain
- Effects varied across age and sex groups

## Repository Structure

- Project_Master_Thesis/
- 
- Data/
- cleaned_dataset_for_the_main_result.csv
- 
- Outputs/
- tables/
- Main_results_table.png
- Demographic_results_table.png
- maps/
- Weather_stations_coverage_per_province.png
- Average_monthly_mortality_rate_by_province.png
- 
- Scripts/
- 01_api_collection/
- PART_1_api.py
- 02_cleaning/
- PART_2_weather_cleaning.py
- PART_3_mortality_cleaning.py
- PART_4_population_cleaning.py
- 03_building_analysis_dataset/
- PART_5_demographics_merging.py
- PART_6_panel_construction.py
- PART_7_merging_all.py
- 04_regression_analysis/
- PART_8_fixed_effects_analysis.py
- PART_9_demographic_analysis.py
- 05_visualization/
- PART_10_geographic_maps.py
- 
- README.md


## Data Availability

This repository contains a curated version of the thesis analysis workflow.

Only a cleaned final analysis dataset (`cleaned_dataset_for_the_main_result.csv`) is included and serves as the basis for the main regression analysis.

Due to dataset size and processing complexity, not all raw, intermediate, robustness-check, demographic-analysis, and geospatial files used in the full thesis are included in this repository. 

The repository is intended to demonstrate the core data pipeline, feature engineering, panel-data construction, fixed effects analysis, and visualization workflow used in the project.

## Reproducibility

Due to external data sources, API-based data collection, and intermediate processing steps, the full workflow is not fully reproducible end-to-end without additional setup and external credentials.
