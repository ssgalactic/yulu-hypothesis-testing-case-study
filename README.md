# Yulu Hypothesis Testing Case Study 🚴‍♂️📊

## About 📖

Yulu is India’s leading micro-mobility service provider offering shared electric cycles for a smooth, affordable, and convenient daily commute. This case study investigates the factors affecting the demand for Yulu’s shared electric cycles, aiming to address recent revenue dips and optimize service delivery.

## Dataset Overview 📊

The dataset includes the following features:

- **datetime**: Date and time of the rental.
- **season**: Season of the year (1: Spring, 2: Summer, 3: Fall, 4: Winter).
- **holiday**: Indicator if the day is a holiday (1: Yes, 0: No).
- **workingday**: Indicator if the day is a working day (1: Yes, 0: No).
- **weather**: Weather condition (1: Clear, 2: Misty, 3: Light Snow/Rain, 4: Heavy Rain/Snow).
- **temp**: Temperature in Celsius.
- **atemp**: Feels-like temperature in Celsius.
- **humidity**: Humidity percentage.
- **windspeed**: Wind speed.
- **casual**: Count of casual users.
- **registered**: Count of registered users.
- **count**: Total rental bikes count.

## Insights 🔍

- **Date Range**: January 1, 2011, to December 19, 2012.
- **Seasonal Distribution**: Most frequent season is Winter.
- **Holiday Impact**: Non-holidays are predominant with only 311 holiday entries.
- **Weather Conditions**: Clear or partly cloudy weather is most common.
- **Temperature**: Mean temperature is 20.23°C; "feels-like" temperature is 23.66°C.
- **Humidity**: Mean humidity is 61.89%.
- **Windspeed**: Average windspeed is 12.8 units.
- **Casual Rentals**: Mean count is around 36.
- **Registered Rentals**: Mean count is approximately 155.
- **Total Rentals**: Mean total rental count is 191.

## Analysis 🧐

### Uni-Variate Analysis

- **Season**: Uniformly distributed across seasons.
- **Holiday**: Predominantly non-holidays (97% of data).
- **Working Day**: Majority of data falls on working days (68%).
- **Weather**: Clear or partly cloudy conditions are most frequent (66%).

### Bi-Variate Analysis

- **Seasonal Trends**: Highest rentals in Fall and Summer; lowest in Spring.
- **Holiday Effect**: Higher rentals on non-holidays.
- **Weather Influence**: Favorable weather correlates with higher rentals.

### Correlation Insights

- **Temperature**: Moderate correlation with casual rentals.
- **Humidity**: Negative correlation with both casual and registered rentals.
- **Rental Types**: Strong positive correlation between casual and registered rentals.
- **Total Rentals**: Highly correlated with registered rentals.

## Hypothesis Testing 🧪

### 1. Effect of Working Day on Rentals
- **Null Hypothesis (H0)**: Working day has no effect on the number of cycles rented.
- **Alternate Hypothesis (Ha)**: Working day does have a significant effect on the number of cycles rented.
- **Result**: p-value = 0.226; Fail to reject H0. Working days do not significantly affect rentals.

### 2. Rentals in Different Seasons
- **Null Hypothesis (H0)**: Number of cycles rented is similar across seasons.
- **Alternate Hypothesis (Ha)**: Number of cycles rented differs across seasons.
- **Result**: p-value = 6.16e-149 (ANOVA) & 2.48e-151 (Kruskal-Wallis); Reject H0. Rentals vary significantly by season.

### 3. Rentals in Different Weather Conditions
- **Null Hypothesis (H0)**: Number of cycles rented is similar in different weather conditions.
- **Alternate Hypothesis (Ha)**: Number of cycles rented differs in different weather conditions.
- **Result**: p-value = 5.48e-42 (ANOVA) & 3.50e-44 (Kruskal-Wallis); Reject H0. Rentals vary significantly by weather conditions.

### 4. Weather Dependency on Season
- **Null Hypothesis (H0)**: Weather is independent of the season.
- **Alternate Hypothesis (Ha)**: Weather is dependent on the season.
- **Result**: p-value = 2.34e-26; Reject H0. Weather and season are dependent on each other.

## Recommendations 🚀

1. **Target Marketing**: Focus on spring and summer with promotions to boost rentals during high-demand periods.
2. **Dynamic Pricing**: Implement pricing strategies to optimize resource use based on demand.
3. **Weather-Based Adjustments**: Adjust bike availability according to weather conditions to maximize rentals.
4. **Promote Registrations**: Encourage casual users to become registered members with discounts and loyalty programs.
5. **Customer Comfort**: Provide amenities like umbrellas and rain jackets.
6. **Weather Integration**: Partner with weather services to provide real-time updates in the rental app.
7. **Maintenance Scheduling**: Conduct regular maintenance before peak seasons.

## Conclusion 🎯

The analysis provides valuable insights into the factors affecting bike rentals, highlighting the importance of weather, season, and user type in shaping demand. Implementing the recommendations can help Yulu optimize its operations and enhance user experience.

## Files

- **[Data Analysis Scripts](./scripts)**: Python scripts used for data analysis.
- **[Jupyter Notebooks](./notebooks)**: Jupyter notebooks with detailed analysis and visualizations.
- **[Results](./results)**: Output files and results from hypothesis tests.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
