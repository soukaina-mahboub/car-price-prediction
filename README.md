# Car Price Analysis and Price Prediction

## Project Overview
This project involves web scraping car data from Avito (Moroccan marketplace) and building a machine learning model to predict car prices based on various features.

## Table of Contents
- [Data Collection](#data-collection)
- [Data Analysis](#data-analysis)
- [Data Preprocessing](#data-preprocessing)
- [Model Building](#model-building)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)

## Data Collection
- Scraped car listings data from Avito using BeautifulSoup
- Collected information including:
  - Car brand and model
  - Price
  - Fuel type
  - Transmission type
  - Fiscal power
  - Year
  - Mileage
  - Location

## Data Analysis
### Dataset Overview
- Total records: 24,776 entries
- Features: 32 columns
- Target variable: Price
- Quantitative variables: 21
- Qualitative variables: 11

### Key Findings
- Most common fuel type: Diesel (91%)
- Manual transmission dominates the market (82%)
- Majority of cars are from local dealerships (80%)
- Model years between 2006-2017 are most prevalent

## Data Preprocessing
1. Missing Value Treatment
   - Dropped columns: Sector, Link
   - Mean imputation: Number of doors
   - Mode imputation: Origin, First hand, Condition

2. Feature Engineering
   - Binning of continuous variables
     - Mileage
     - Fiscal power
     - Model year
   - Encoding categorical variables
     - One-hot encoding for fuel type, origin
     - Label encoding for model, brand
     - Binary encoding for transmission, first hand

## Model Building
- Algorithm: Linear Regression
- Train-test split: 80-20
- Features used: All processed variables after encoding

## Validation
- R² Score
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)

## Technologies Used
- Python 3.x
- Libraries:
  - BeautifulSoup4 (web scraping)
  - Pandas (data manipulation)
  - NumPy (numerical operations)
  - Scikit-learn (machine learning)
  - Matplotlib/Seaborn (visualization)

