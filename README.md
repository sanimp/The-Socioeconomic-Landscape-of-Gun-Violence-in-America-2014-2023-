# The Socioeconomic Landscape of Gun Violence in America (2014–2023)

## A State-Level Analysis of Socioeconomic Drivers

**Published:** April 27, 2026  
**Author:** Priscilla Sarfoa Anim  

---

## Project Overview

Gun violence remains one of the most pressing public health crises in the United States. This project investigates how socioeconomic conditions — particularly **poverty rates, household income, and housing costs** — relate to gun violence across U.S. states and counties between **2014 and 2023**.

Using data from the **Gun Violence Archive (GVA)** and the **American Community Survey (ACS)**, this analysis combines:

- Exploratory Data Analysis (EDA)
- Geographic and spatial analysis
- Interactive mapping
- String manipulation techniques
- Statistical testing
- Population-adjusted violence metrics

The findings provide strong statistical evidence that states with higher poverty rates experience significantly higher gun violence rates.

---

# Table of Contents

- [Introduction](#-introduction)
- [Project Objectives](#-project-objectives)
- [Datasets](#-datasets)
- [Data Dictionary](#-data-dictionary)
- [Tools & Libraries](#-tools--libraries)
- [Data Cleaning](#-data-cleaning)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [String Manipulation](#-string-manipulation)
- [Interactive Maps](#-interactive-maps)
- [Geographic Analysis](#-geographic-analysis)
- [Merging Data Sets](#-merging-data-sets)
- [Summary Statistics](#-summary-statistics)
- [Data Visualizations](#-data-visualizations)
- [Permutation / Randomization Test](#-permutation--randomization-test)
- [Key Findings](#-key-findings)
- [Conclusions](#-conclusions)
- [Policy Implications](#-policy-implications)
- [Project Structure](#-project-structure)
- [How to Run the Project](#-how-to-run-the-project)
- [Contributions](#-contributions)

---

# Introduction

Gun violence affects thousands of individuals and communities across the United States every year. While the social and political dimensions of gun violence are widely discussed, the socioeconomic factors driving geographic disparities are often less understood.

This project explores whether economic disadvantage — especially poverty — is associated with higher gun violence rates across the United States from **2014–2023**.

By merging incident-level gun violence records with county-level socioeconomic indicators, the project identifies both geographic and temporal patterns while testing whether poverty is a statistically significant predictor of gun violence.

---

# Project Objectives

This project aims to:

1. Analyze geographic patterns of gun violence across U.S. states  
2. Investigate relationships between poverty and gun violence rates  
3. Compare high-poverty vs. low-poverty states  
4. Build interactive and static visualizations  
5. Apply string manipulation techniques to real-world text data  
6. Perform statistical inference using a permutation test  
7. Create population-adjusted gun violence metrics  

---

# Datasets

## 1 Gun Violence Archive (GVA)

A nationwide dataset containing gun violence incidents across the United States.

### Key Variables
- Incident date
- State and city
- Victims killed/injured
- Suspects killed/injured
- Incident characteristics
- Geographic coordinates

---

## 2 American Community Survey (ACS)

County-level socioeconomic and demographic estimates from the U.S. Census Bureau.

### Key Variables
- Population
- Median household income
- Poverty rate
- Housing costs
- Gender proportions

---

# Data Dictionary

## Gun Violence Dataset (`gun_violence_geo.csv`)

| Variable | Description |
|---|---|
| geoid | County FIPS code |
| incident_id | Unique incident identifier |
| date | Incident date |
| state | U.S. state |
| city | City |
| county | County |
| latitude | Latitude coordinate |
| longitude | Longitude coordinate |
| number_victims_killed | Victims killed |
| number_victims_injured | Victims injured |
| number_suspects_killed | Suspects killed |
| number_suspects_injured | Suspects injured |
| incident_characteristics | Description of incident |

---

## ACS Dataset (`census_data_county_2009-2023.csv`)

| Variable | Description |
|---|---|
| geoid | County FIPS code |
| county_state | County and state |
| year | ACS survey year |
| population | County population |
| median_income | Median household income |
| median_monthly_rent_cost | Median monthly rent |
| median_monthly_home_cost | Median monthly housing cost |
| prop_poverty | Poverty proportion |
| prop_female | Female population proportion |
| prop_male | Male population proportion |

---

# Tools & Libraries

This project was completed in **R** using the following libraries:

```r
library(tidyverse)
library(sf)
library(tigris)
library(leaflet)
library(lubridate)
library(skimr)
library(naniar)
library(flextable)
library(gt)
library(gtExtras)
library(scales)
library(janitor)
library(calendR)
library(maps)
