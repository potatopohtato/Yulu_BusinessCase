# README: Yulu Business Case Analysis

## Overview
This repository contains the analysis and findings for Yulu, India's leading micro-mobility service provider, to understand the factors influencing the demand for shared electric cycles in the Indian market. The goal of this analysis is to identify significant variables that predict demand and provide actionable recommendations to address the revenue dip experienced by Yulu.

## Problem Statement
Yulu aims to identify the key factors that influence the demand for shared electric cycles in the Indian market. The analysis focuses on understanding which variables significantly predict demand and how well these variables explain the observed trends in cycle rentals.

### Key Questions:
1. Which variables significantly predict the demand (i.e., count)?
2. How well do these variables explain the observed trends in demand?

## Dataset
The dataset used for this analysis is `bike_sharing.csv`, which contains hourly data on bike rentals, including variables such as:
- **datetime**: Date and time of the rental.
- **season**: Season (1: spring, 2: summer, 3: fall, 4: winter).
- **holiday**: Whether the day is a holiday.
- **workingday**: Whether the day is a working day.
- **weather**: Weather conditions (1: Clear, 2: Mist/Cloudy, 3: Light Snow/Rain, 4: Heavy Rain/Snow).
- **temp**: Temperature in Celsius.
- **atemp**: "Feels like" temperature in Celsius.
- **humidity**: Humidity percentage.
- **windspeed**: Wind speed.
- **casual**: Count of casual users.
- **registered**: Count of registered users.
- **count**: Total count of rented bikes (casual + registered).

## Analysis Steps
1. **Data Loading and Cleaning**:
   - Imported necessary libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`).
   - Loaded the dataset and checked for missing values and duplicates.
   - Converted the `datetime` column to a datetime object and extracted useful components (hour, day, month, year).
   - Converted categorical variables (`season`, `holiday`, `workingday`, `weather`) to the category data type.

2. **Univariate Analysis**:
   - Plotted histograms and boxplots for numerical variables (`temp`, `atemp`, `humidity`, `windspeed`) to understand their distribution and detect outliers.
   - Created countplots for categorical variables (`season`, `holiday`, `workingday`, `weather`) to understand their frequency distribution.

3. **Bivariate Analysis**:
   - Analyzed the relationship between `count` (total rentals) and other variables using boxplots.
   - Examined the correlation between numerical variables using a correlation matrix and heatmap.

4. **Hypothesis Testing**:
   - **T-Test**: Tested whether working days affect the number of electric cycles rented.
   - **ANOVA**: Tested whether weather or season affects the number of cycles rented.
   - **Chi-Square Test**: Tested whether weather is dependent on season.

## Key Findings
1. **Working Days vs. Non-Working Days**:
   - There is no significant difference in the number of cycles rented between working and non-working days.

2. **Seasonal Impact**:
   - The season does not significantly affect the number of cycles rented.

3. **Weather Impact**:
   - Weather has a significant effect on the number of cycles rented. Light rain and snow decrease rentals significantly, while heavy rain or snow drastically reduces rentals.

4. **Weather and Season Dependency**:
   - Weather is dependent on the season, meaning certain weather conditions are more likely to occur in specific seasons.

## Recommendations
Based on the analysis, the following recommendations are provided to Yulu to improve business performance:

1. **Optimize Pricing and Availability for Working Days**:
   - Consider adjusting pricing models or increasing cycle availability during non-working days to attract more users.

2. **Seasonal Promotions**:
   - Develop marketing campaigns or incentives targeting specific seasons (e.g., spring) to drive more rentals.

3. **Improve Infrastructure Based on Weather and Season Trends**:
   - Ensure the availability of cycles in high-demand weather conditions and seasons by positioning bikes in high-footfall areas like metro stations or business hubs.

4. **Monitor Working Day Performance**:
   - Focus on improving the user experience for delivery partners, Q-Commerce couriers, and students by increasing the number of cycles near restaurants, colleges, business parks, and metro stations.

## Conclusion
This analysis provides insights into the factors influencing the demand for Yulu's shared electric cycles. By focusing on weather conditions and optimizing operations based on seasonal trends, Yulu can improve its service offerings and increase revenue.

## Files
- **`yulu-businesscase.pdf`**: Contains the detailed analysis, visualizations, and findings.
- **`cleaned_yulu_data.csv`**: The cleaned dataset used for analysis.

## Dependencies
- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`

## How to Run the Analysis
1. Install the required libraries using `pip install -r requirements.txt`.
2. Run the Jupyter Notebook or Python script to reproduce the analysis.

## Author
[Your Name]

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
