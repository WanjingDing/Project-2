# Sickle Cell Disease and Air Pollution Analysis
## Project Overview
This project analyzes the relationship between air pollutants and sickle cell disease (SCD) in Durham County, North Carolina. The analysis processes raw air quality data from the EPA and creates visualizations to explore seasonal patterns and trends in pollutant concentrations (CO, PM2.5, and O3) from 2018-2020.

**Author:** Wanjing Ding  
**Course:** BIOSTAT 721  
**Date:** November 17 2025  

## Data Sources
- **Air Quality Data:** EPA air quality monitor at RDU Airport
- **Time Period:** January 2018 - April 2020
- **Pollutants Measured:**
  - Carbon Monoxide (CO) - Daily Max 8-hour concentration
  - Fine Particulate Matter (PM2.5) - Daily mean concentration
  - Ozone (O3) - Daily Max 8-hour concentration

## Repository Contents
```
├── Ding_Wanjing_Project2.Rmd      # Main RMarkdown analysis file
├── air_quality_2018.csv            # 2018 air quality data
├── air_quality_2019.csv            # 2019 air quality data
├── air_quality_2020.csv            # 2020 air quality data (Jan-Apr only)
└── README.md                       # This file
```

## Requirements
### Software
- R
- RStudio
### R Packages
```r
library(tidyverse)  # Data manipulation and visualization
library(lubridate)  # Date handling
library(readr) # Read data
library(here) # Read data
library(ggplot2) # Creating plots
```

### Running the Analysis
### `process_air_quality(df)`
Processes raw air quality data with the following steps:
- Renames pollutant concentration columns to shorter, standardized names
- Converts date strings to proper Date format
- Calculates daily averages for days with multiple measurements
- Removes duplicate rows
- Sets negative concentration values to zero
## Analysis Components
### 1. Data Processing
- Combined three years of air quality data (2018-2020)
- Handled duplicate measurements by averaging
- Corrected measurement errors (negative values)
- Formatted dates consistently
### 2. Visualizations
#### Plot 1: Monthly CO and O3 Concentrations
- Monthly averages across all three years
- 95% confidence interval error bars
- Separate y-axes for each pollutant (faceted)
- Displays seasonal patterns
#### Plot 2: Monthly PM2.5 Concentrations by Year
- Year-by-year comparison (2018, 2019, 2020)
- Shows temporal trends
- Note: 2020 data only available through April

## Key Findings

### Seasonal Patterns
- **CO:** Higher concentrations in winter months (Dec-Jan), lower in summer (May-Aug)
- **O3:** Peak concentrations in summer months, consistent with photochemical formation
- **PM2.5:** Elevated levels in winter, lower in spring/summer
