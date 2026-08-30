# California Pollution & Mortality Analysis

## Overview
This project analyzes the relationship between air pollution (ozone, PM2.5, AQI) and 
mortality across California counties using daily monitor-level data from 2024. The 
analysis covers data cleaning and merging, descriptive statistics, visualization, and 
panel regression models with fixed effects — with particular attention to the 
identification threats that complicate a causal interpretation of the results.

## What's in this repo
- **Data processing**: Merges two monitor-level datasets (ozone and PM2.5) on 
  county, site, and date; reconciles inconsistent formatting (county codes, date types); 
  collapses to a county-day panel by averaging across monitors.
- **Descriptive statistics**: Summary tables for ozone, PM2.5, and AQI, including a 
  breakdown by data source (EPA AQS vs. AirNow) with a discussion of what summary 
  statistics can and can't reveal about underlying data quality.
- **Visualization**: Standardized distribution comparison of ozone and PM2.5; a 
  county-level daily time series used to assess autocorrelation.
- **Regression analysis**: Two-way (county × date) fixed-effects models of mortality 
  on AQI, including a lagged-pollution specification and a CBSA interaction term, with 
  discussion of collinearity and omitted variable bias.
- **Identification discussion**: A written analysis of threats to causal interpretation, 
  including omitted lag structure, unobserved county-day confounders, and mortality 
  "harvesting" (short-term displacement vs. genuine increases in mortality).

## Tools
Python — `pandas`, `numpy`, `statsmodels`, `matplotlib`

## Data
Daily county-monitor-day pollution readings (ozone, PM2.5, AQI) for California in 2024, 
merged with a synthetic mortality variable for analytical purposes.

*Note: the mortality data used here are synthetic and constructed for the purposes of 
this exercise; they are not real mortality records.*
