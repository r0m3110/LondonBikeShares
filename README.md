# London Bike Shares
## Background

**Company Overview:**
Transport for London (TfL) is a government organization responsible for managing public transportation and road systems in London, UK. Established in 2000, TfL operates within the transportation industry, focusing on providing efficient, sustainable, and accessible travel options. Its diverse portfolio includes buses, underground trains, overground railways, and initiatives to promote cycling.

**Business Model:**
TfL’s bike-sharing program is designed to promote eco-friendly travel and reduce traffic congestion. By placing docking stations strategically across London, the program ensures ease of access and encourages short-duration rides. This operational model optimizes bike availability and aligns with TfL’s broader goals of reducing carbon emissions and promoting health and fitness among residents.

To achieve these goals, TfL prioritizes enhancing operational efficiency by reducing docking station shortages during peak times through accurate demand prediction and optimized bike redistribution schedules. Additionally, the program focuses on increasing bike utilization rates by addressing factors that limit access, such as poor weather or station overcrowding. Promoting user satisfaction remains a key priority, with efforts aimed at improving service accessibility and responding to user feedback to deliver a seamless bike-sharing experience.

## Key Business Metrics:

Bike Rentals: The total number of rides completed over a given period.

Utilization Rates: The percentage of bikes in active use at any given time.

Operational Efficiency: Metrics such as docking station availability and bike redistribution times.

Customer Satisfaction: Measured through user feedback, return rates, and service accessibility.

Environmental Impact: Reduction in CO2 emissions as a result of increased bike usage.

As a data analyst at TfL, I focus on leveraging these metrics to optimize operations, predict usage trends, and provide actionable insights that enhance service delivery and user satisfaction. By analyzing historical data and external factors like weather and holidays, I support strategic decision-making to ensure the bike-sharing program remains a reliable and sustainable travel option for Londoners.

Insights and recommendations are provided on the following key areas:

**Category 1: Hourly Patterns**

**Category 2: Weekly Trends**

**Category 3: Seasonal Trends**

**Category 4: Weather Impact**

The Python queries used to inspect and clean the data for this analysis can be found here [link].

Targed Python queries regarding various business questions can be found here [link].

An interactive Tableau dashboard used to report and explore sales trends can be found here [link].

## Data Structure & Initial Checks
The main database structure consists of a single table with a total of 17,414 records. This table captures detailed hourly bike-sharing data, weather conditions, and temporal information. A description of the table and its key columns is as follows:

Main Table: Bike Sharing Data
time: Timestamp of the recorded data, grouped hourly.
count: Total number of bike rentals during the corresponding time interval.
temp_real_C: Actual temperature in Celsius.
temp_feels_like_C: Perceived temperature in Celsius.
humidity: Humidity levels as a percentage.
wind_speed_kph: Wind speed in kilometers per hour.
weather: Weather conditions (e.g., clear, broken clouds, rain).
is_holiday: Binary indicator of whether the day is a holiday (1 = holiday, 0 = non-holiday).
is_weekend: Binary indicator of whether the day falls on a weekend (1 = weekend, 0 = weekday).
season: Seasonal category (spring, summer, fall, winter).
Initial Checks
The table has no missing values, ensuring completeness of the dataset.
Columns have been cleaned and converted into appropriate data types (e.g., time to datetime, categorical variables encoded as strings or integers).
Key temporal columns, such as time and season, were used to extract derived features like hour and weekday for further analysis.

## Insights Deep Dive

Hourly Patterns

Main Insight 1: Peak hours for bike rentals occur at 8:00 AM, 5:00 PM, and 6:00 PM, with average rentals of 2882, 2829, and 2629 respectively. This reflects strong demand during commuter rush hours. Operational efforts should ensure sufficient bike availability during these times to reduce user dissatisfaction.

Main Insight 2: Off-peak hours, particularly between 3:00 AM and 5:00 AM, see significantly lower rentals, averaging fewer than 110 rides per hour. These periods may represent opportunities to focus redistribution efforts or conduct maintenance without impacting users.

[Visualization: Hourly Rentals Trends]

Weekly Trends

Main Insight 1: Rentals peak midweek, with Thursday showing the highest average of 1258 rentals, followed by Wednesday and Tuesday. This suggests commuting patterns drive demand during weekdays.

Main Insight 2: Weekend rentals are comparatively lower, with Sunday averaging 959 rentals and Saturday 995 rentals. Marketing campaigns could encourage leisure usage during these days to balance demand.

[Visualization: Average Rentals by Day of the Week]

Seasonal Trends

Main Insight 1: Summer is the most active season, averaging 1464 rentals, while winter experiences the lowest demand at 821 rentals. This highlights the influence of weather and daylight on bike usage. Winter promotions or operational adjustments may help mitigate low demand.

Main Insight 2: Spring and autumn show moderate activity, averaging 1103 and 1178 rentals respectively. These seasons can serve as benchmarks for assessing weather-dependent fluctuations.

[Visualization: Seasonal Rental Trends]

Weather Impact

Main Insight 1: Clear weather and scattered clouds result in the highest rentals, averaging 1162 and 1496 respectively. Conversely, snowfall and thunderstorms drastically reduce rentals, averaging 250 and 583.

Main Insight 2: Rainy conditions (712 rentals on average) show moderate usage, indicating that some users may still rely on bikes despite adverse weather. Providing protective gear or targeted campaigns could enhance ridership in such conditions.

[Visualization: Weather Condition Impact on Rentals]

Recommendations

Based on the insights and findings above, we would recommend the stakeholder team to consider the following:

Observation: Peak rental hours occur at 8:00 AM, 5:00 PM, and 6:00 PM, driven by commuter activity.
Recommendation: Ensure adequate bike availability and docking capacity at major commuter hubs during these times to prevent shortages and maximize customer satisfaction.

Observation: Weekend rentals are significantly lower compared to weekdays, averaging under 1000 rentals.
Recommendation: Develop promotional campaigns or leisure-oriented events to boost weekend ridership, such as discounts or partnerships with local attractions.

Observation: Winter sees the lowest bike rental activity, with an average of 821 rentals compared to 1464 in summer.
Recommendation: Introduce winter-specific incentives, such as discounts on memberships or partnerships with weather-appropriate gear providers, to encourage ridership during colder months.

Observation: Clear weather and scattered clouds result in the highest rentals, while snowfall and thunderstorms significantly reduce demand.
Recommendation: Use predictive weather models to adjust bike availability dynamically, ensuring resources are allocated effectively during high-demand conditions.

Observation: Off-peak hours between 3:00 AM and 5:00 AM experience minimal demand.
Recommendation: Schedule maintenance and redistribution efforts during these hours to minimize service disruptions and optimize operations.

Assumptions and Caveats:

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

Assumption: Missing values were assumed to be negligible since no missing information was identified during the initial data checks. If any missing data were present, they were assumed not to significantly affect the analysis due to the dataset’s large size.

Assumption: Weather condition codes and descriptions were accurately mapped to their respective rental trends. It was assumed that no overlapping or incorrectly labeled conditions exist in the data.

Assumption: Holidays and weekends were correctly classified. The dataset’s boolean indicators (‘is_holiday’ and ‘is_weekend’) were presumed to align with standard UK public holidays and calendar weekends.

Caveat: External factors such as city-wide events, strikes, or unplanned disruptions were not included in the dataset, which may affect the rental counts during certain periods.

Assumption: Historical data from 2015 and 2016 were representative of typical bike-sharing trends, even though social or environmental changes might alter these patterns in future years.
