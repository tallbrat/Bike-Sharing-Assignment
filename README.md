# Bike Sharing Assignment
This analysis aims to identify and quantify the key factors driving demand for shared bikes in the US market. By building a predictive model using linear regression, we will uncover actionable insights that BoomBikes can leverage to optimize its business strategies, such as bike availability and pricing, and guide potential expansion into new markets.

## Table of Contents
* [General Info](#general-information)
* [Conclusions](#conclusions)
* [Model Comparison](#model-comparison)
* [Technologies Used](#technologies-used)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- What is the background of your project?
> This project is part of the IIITB PGDM program in ML & AI, focusing on skills in Exploratory Data Analysis (EDA) and building a Linear Regression model.
- What is the business probem that your project is trying to solve?
>The goal is to identify and quantify key factors influencing shared bike demand in the US market. This predictive analysis will help guide strategies for optimizing bike availability, pricing, feature building and possible market expansion.
- What is the dataset that is being used?
> The dataset, day.csv - provides daily cumulative rental data spanning two years, capturing patterns in bike demand and other relevant variables.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
### 1. Predictive Features:
- **Previous Day’s Demand:** Both models consistently identified previous day's demand (previous_day_diff) as a primary driver, suggesting that usage trends and demand continuity play a key role in predicting future demand.
- **Temperature and Heat Index:** Model 4 highlighted temperature, while Model 5 introduced the heat index as a strong indicator of demand, indicating that comfortable weather conditions (moderate temperatures) are conducive to higher usage.
- **Year-on-Year Increase:** The year variable was significant in both models, reflecting potential growth in market acceptance or expanding user adoption over time.

### 2. Seasonal and Monthly Impact:
- **Seasonality:** Both models showed that winter positively influences demand, while spring shows a slight negative impact. This suggests that BoomBikes may consider promoting off-season bike use in spring to balance seasonal dips.
- **Monthly Patterns:** Model 5, with a more detailed breakdown of months, showed higher demand in months like September, May, October, and March. This granular view could enable BoomBikes to optimize pricing and availability for peak months.

### 3. Negative Influences:
- **Humidity and Wind Speed:** High humidity and wind speed were consistently associated with lower demand across both models. BoomBikes can leverage this insight to adjust forecasts and supply dynamically based on weather patterns.
- **Weather Conditions:** Both models show a decline in demand on days with adverse weather, such as light snow or rain. To address this, BoomBikes could introduce features like grippier tires, a lightweight protective roof, and sheltered bike parking areas. These additions would allow riders to wait out light rain comfortably before resuming their journey with easily accessible protective bikes.

## Model Comparison
- **Model 4** is simpler, factoring in fewer monthly and weekday variations, which may make it easier to interpret but potentially less accurate in capturing demand variability due to monthly influences.
- **Model 5**, with more extensive monthly detail, offers a more precise reflection of demand trends across different times of the year, potentially aiding BoomBikes in optimizing inventory and marketing efforts on a month-by-month basis. 
- Despite this, both models show similar predictive performance, with marginal differences in MSE and R-squared.


## Technologies Used
- python - version 3+
    - numpy
    - pandas
    - matplotlib
        - pyplot
    - seaborn
    - sklearn
        - model_selection.train_test_split
        - preprocessing.MinMaxScaler
        - feature_selection.RFE
        - linear_model.LinearRegression
        - metric
            - mean_squared_error
            - r2_score
    - statsmodels
        - api
        - stats
            - diagnostic.het_breuschpagan
            - outliers_influence.variance_inflation_factor
        - graphics.tsaplots.plot_acf
    - scipy
        - stats
- warnings

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- This project was inspired by upGrad IIITB ML & AI PGDM programme.
- This project was based on EDA and Multiple Linear Regression.


## Contact
Created by [@tallbrat] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->