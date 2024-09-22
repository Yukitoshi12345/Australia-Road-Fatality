<h1 align = "center"> Australia Road Fatality </h1>

Fatal crashes: each record is a fatal crash. Details include year, month, day of week, time, location, crash type, and involvement of particular vehicle types.

## Table of Contents

- [Data](#data)
- [Libraries Used](#libraries-used)
- [Results](#results)
- [References](#references)
- [License](#license)

## Data

| Column                        | Description                                                                                                                                                                              |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Crash ID                      | A unique identifier for each crash in the dataset. It helps distinguish between different crashes.                                                                                       |
| State                         | The state or territory where the crash occurred (e.g., NSW, QLD). This helps geographically categorise crashes.                                                                          |
| Month                         | The month in which the crash occurred, represented numerically (1 for January, 2 for February, etc.).                                                                                    |
| Year                          | The year the crash occurred. It allows for time-based analysis and trend identification over years.                                                                                      |
| Dayweek                       | The day of the week when the crash occurred (e.g., Monday, Friday). This is useful for analysing patterns related to specific days.                                                      |
| Time                          | The time of day the crash occurred, typically in 24-hour format (e.g., 14:00 for 2 PM). It helps assess whether crashes are more likely at specific times.                               |
| Bus Involvement               | Indicates whether a bus was involved in the crash (Yes/No). This is useful for understanding the involvement of public transport.                                                        |
| Heavy Rigid Truck Involvement | Indicates whether a heavy rigid truck (a large truck) was involved in the crash (Yes/No).                                                                                                |
| Articulated Truck Involvement | Indicates whether an articulated truck (like a semi-trailer or long-haul truck) was involved (Yes/No).                                                                                   |
| Speed Limit                   | The speed limit (in km/h) of the road where the crash occurred. This can help determine if speed limits were a factor in crashes.                                                        |
| Road User                     | Describes the type of road user involved in the crash (e.g., pedestrian, driver, motorcyclist). This helps classify the type of participants in the crash.                               |
| Gender                        | The gender of the person involved in the fatality (Male/Female). This is useful for demographic analysis of fatalities.                                                                  |
| Age                           | The age of the person involved in the crash. It provides further demographic insights into the people involved in fatal crashes.                                                         |
| National Remoteness Areas     | Classifies the location of the crash based on the remoteness of the area (e.g., Major Cities, Inner Regional, Outer Regional, etc.). This helps analyse urban vs. rural crashes.         |
| SA4 Name 2021                 | Statistical Area Level 4, a geographic region based on the 2021 census, representing large regions in Australia. This gives detailed geographic information.                             |
| National LGA Name 2021        | Local Government Area name based on 2021 census data. This provides a finer geographic classification.                                                                                   |
| National Road Type            | The classification of the road type where the crash occurred (e.g., Arterial Road, Collector Road, Sub-arterial Road). It helps to understand the infrastructure where crashes occurred. |
| Christmas Period              | Indicates whether the crash occurred during the Christmas holiday period (Yes/No). Useful for analysing seasonal effects on crashes.                                                     |
| Easter Period                 | Indicates whether the crash occurred during the Easter holiday period (Yes/No).                                                                                                          |
| Age Group                     | Groups the ages of the individuals involved into categories (e.g., 18 to 25, 40 to 64). This is helpful for broader demographic analysis.                                                |
| Day of week                   | Indicates whether the crash occurred on a weekday or weekend. This categorisation helps in analysing crash patterns across workdays and weekends.                                        |
| Time of day                   | Groups the crash time into broad categories like "Day" or "Night" to identify time-based patterns in fatalities.                                                                         |

## Libraries Used

- pandas
- numpy
- matplotlib
- scipy.stats

## Results

<b> Q1: What is the general trend for road fatalities in Australia over the past 35 years? </b>

![](images/road_fatalities_trend.png)

The graph shows the trend of total road crashes in Australia from 1989 to 2023, with a clear overall downward trend in the number of crashes. Below is a detailed summary and analysis based on the visualisation:

1. Significant Decrease in Road Crashes Over Time:
- In 1989, there were approximately 2800 crashes per year.
- By 2023, this number has decreased to about 1269 crashes, representing a reduction of over 50% in road crashes during the 35-year period.
- The most substantial reduction occurred between 1989 and 1992, where crashes dropped from 2800 to 1974.

2. Fluctuations in Decline:
- The overall trend is downward, but there are periods of stability and slight increases:
    - After the sharp decline between 1989 and 1992, crashes stabilised around 1900-2000 crashes per year between 1992 and 1997.
    - From 1998 to 2010, there was a continued decrease in crashes, with numbers dropping from 1755 in 1998 to a low of 1277 in 2011.
    - Post-2011, crashes continued to decline, reaching a low of 1097 crashes in 2020.
- After 2020, there was a slight uptick in crashes, rising to 1269 in 2023.

3. Implications of the Decline:
- The consistent reduction in road crashes can likely be attributed to several factors:
    - Improved road safety measures: Better road infrastructure, stricter traffic law enforcement, and increased awareness of road safety likely contributed to this reduction.
    - Technological Advances: The development of safer vehicle technologies (such as airbags, anti-lock braking systems, and electronic stability control) likely played a significant role.
    - Government intervention: Policies such as lower speed limits, mandatory seatbelt usage, and zero-tolerance for drink-driving helped reduce crashes.

4. Recent Stability and Slight Uptick:
- In the years between 2020 and 2023, there was a slight rise in the number of crashes, increasing from 1097 crashes in 2020 to 1269 in 2023.
- This recent increase could be due to the rebound effect post-pandemic, as more vehicles returned to the road following COVID-19 restrictions. It may also be driven by new factors such as distractions from mobile devices or other technological impacts.

Summary

- The data show that road safety in Australia has significantly improved over the last 30 years, with crashes decreasing by over 50%, from 2800 in 1989 to 1269 in 2023.
- While much of this reduction can be attributed to advancements in safety technology, better driver education, and stronger laws, the slight rise in recent years warrants further investigation.

Statistical Insights

- Time Series Analysis: The long-term downward trend suggests that safety measures have had a substantial positive impact in reducing crashes.
- Comparison: Comparing the peak crash periods of the early 1990s with the most recent years highlights a dramatic improvement in road safety.
- Correlation: Further analysis could explore the relationship between crash trends and external factors, such as changes in vehicle technology, traffic enforcement policies, or driver behaviour over the years.

<br>

<b> Q2: Anova test: Did the variance in monthly road fatalities differ significantly between Australian states during the COVID-19 lockdown period (March 2020 to December 2021)? </b>

- Null Hypothesis (H0): The variance in monthly road fatalities between Australian states during the COVID-19 lockdown period is the same.
- Alternative Hypothesis (H1): There is a significant difference in the variance of monthly fatalities between at least two Australian states during the lockdown.

Box Plot: Distribution of Monthly Road Fatalities Across States

![](images/covid_monthly_avg_states.png)

- Key Insights:
    - The box plot shows the distribution of monthly fatalities of each state. NSW and VIC exhibit broader ranges of fatalities, while states like TAS and NT show narrower ranges.
    - Outliers can be observed in several states, indicating months where fatalities significantly deviated from the median.
- Implications:
    - This visualisation highlights that the distribution of fatalities differs between states, suggesting that factors such as state-specific lockdown measures or traffic patterns may have impacted fatalities differently.


Time Series Plot: Monthly Road Fatalities Over Time Across States

![](images/covid_monthly_states.png)

- Key Insights:
    - This plot shows how fatalities evolved month by month for each state. States like NSW and VIC experienced noticeable fluctuations, particularly in late 2020 and early 2021, whereas states like Tasmania had more stable patterns.
- Implications:
    - The temporal trend helps identify periods where road fatalities either spiked or declined, reflecting potential impacts of varying lockdown policies and public health restrictions.
    - Splitting the time series into individual state subplots improves clarity, making it easier to track trends within each state.
    
ANOVA Results
- F-value: 54.74
- p-value: 7.46 × 10^−25
 
Key Statistical Findings:
- The p-value is significantly lower than 0.05, indicating that we reject the null hypothesis. This means there is a statistically significant difference in the variance of monthly road fatalities across Australian states during the COVID-19 lockdown.
- The F-value of 54.74 further supports that the differences in variances are substantial across the states.

- Findings from Visualisations:
    - The box plot and bar chart clearly show that states like NSW and VIC had higher and more varied road fatalities compared to smaller states such as TAS and NT.
    - The time series plot and heatmap reveal that fatalities not only differed by state but also fluctuated across different months during the lockdown.

- Statistical Analysis:
    - The ANOVA test confirmed that the variance in monthly fatalities was not consistent across states, with significant differences observed between them. This suggests that factors like lockdown stringency, traffic enforcement, and road conditions likely varied significantly from state to state.

- Professional Implications:
    - The findings suggest that targeted interventions could have been more effective if tailored to individual states' conditions, such as more stringent road safety campaigns or traffic law enforcement during high-risk months.
    - Understanding the temporal and state-wise variance in road fatalities can help policymakers and traffic safety officials develop more region-specific strategies for improving road safety during future crises or restrictions.

Conclusion:
The analysis of monthly road fatalities across Australian states during the COVID-19 lockdown period revealed substantial differences in both the distribution and trends of fatalities between states. Supported by visualizations and the ANOVA test, it is evident that these differences are statistically significant. Policymakers and public safety officials may benefit from considering these insights when addressing state-specific traffic safety measures in similar situations moving forward.








<br>

<b> Q3: Specifically in the last four years, is there a trend regarding various factors (speed limits, age, time of the day, day of the week, & type of road) as related to the number of fatalities? </b>

<br>

<b> Q4: Specifically in Victoria, did the introduction of booze buses and mobile speed radars have a significant impact on road fatalities? </b>

<br>

<b> Q5: In 1999, Victoria rewrote various road regulations. Did this change have a significant impact on road fatalities? How did this compare to NSW across the same period? </b>

## References

https://www.bitre.gov.au/statistics/safety/fatal_road_crash_database

## License

This project is licensed under the [MIT License](https://github.com/Yukitoshi12345/Australia-Road-Fatality/blob/main/LICENSE).
