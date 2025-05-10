# Uber Taxi Ride Analysis Dashboard (Power BI)
This project presents an interactive Power BI dashboard analyzing Uber taxi ride data. It explores ride frequency, fare revenue, trip durations, distances, and night shift patterns to uncover operational insights for taxi services.

The project follows a structured end-to-end process: from data cleaning to data modeling, DAX measures, visualizations, and dashboard creation.

## Objective
To design a business intelligence dashboard that provides meaningful insights into taxi ride operations, enabling data-driven decision-making for operational and marketing strategies.

## Business Questions and KPIs
* How many trips were completed in a selected timeframe?
* What was the total fare revenue generated?
* How much total distance and duration were covered?
* What proportion of trips happened during night hours?
* How do trips vary by day of the week and by pickup time?
* Which locations have the most taxi activity?
* What payment methods were most commonly used?

## Tools and Technologies Used
* Power BI: Data Modeling, Visualization, DAX calculations
* Power Query: Data cleaning and transformation

## Process Followed
### 1. Data Collection
* <a href="https://github.com/RichaAV/uber-taxi-ride-analysis/blob/main/trip-details.xlsx">Trip Details.xlsx</a> containing trip-level records (fare amount, trip distance, pickup datetime, payment type, etc.)
* <a href="https://github.com/RichaAV/uber-taxi-ride-analysis/blob/main/location-table.csv">Location Table.csv</a> mapping location IDs to location names.

### 2. Data Cleaning (Power Query)
* Removed unnecessary columns.
* Handled missing/null values.
* Merged Trip Details and Location Table based on location IDs to enrich data with location names.
* Formatted datetime fields for proper temporal analysis.

### 3. Data Modeling
* Established relationships between Trip and Location tables.
* Set appropriate data types for fields (dates, numerics, categories).
* Created a star schema for optimal report performance.

### 4. DAX Measures Creation
* Total Trips = Count of Trip IDs
* Total Fare = Sum of Fare Amount
* Total Distance = Sum of Trip Distance
* Total Duration = Sum of Trip Duration
* Night Shift Trips % = Percentage of trips happening between 8 PM and 6 AM
* Additional time intelligence measures for day and shift analysis.

### 5. Data Visualization
* KPI Cards for Total Trips, Total Fare, Total Duration, Total Distance, and Night Trip %
* Slicers (Filters) for Month, Day Name, and Location
* Bar charts for Total Trips by Location
* Donut charts for Shift and Payment Type distribution
* Line chart for Total Trips by Day of the Week
* Area chart for Trips by Pickup Time (binned)
* Drill-through pages for detailed location and day analysis
* <a href="https://github.com/RichaAV/uber-taxi-ride-analysis/blob/main/dashboard_image.png" target=_blank">View Dashboard</a>

## Key Insights
* 117K total trips were recorded within the data period.
* $1.8M in total fare revenue was generated.
* 1.9 million minutes of total trip time accumulated.
* 393.9K kilometers/miles of total distance traveled.
* 8.7% of trips occurred during night shifts, indicating demand at night.
* Upper East Side North and East Harlem South were the top pickup locations.
* Cash payments remained the dominant mode, but digital payments (Uber Pay, Google Pay) showed noticeable usage trends.
* Saturdays and Sundays witnessed the highest number of rides, while mid-week (especially Thursday) saw a dip.
* Peak trip times were observed between 7 AM to 9 AM and 5 PM to 8 PM, aligning with typical commuting hours.

## Conclusion
* The dashboard successfully captures and visualizes key operational metrics for Uber/Ola taxi services. It enables stakeholders to:
* Identify top-performing locations
* Understand peak ride times and days
* Analyze fare revenues across different time windows
* Recognize the share of night-time rides for potential service optimization

The modular design and interactive filters make it easy to drill down into specific days, months, or locations for deeper analysis. Future enhancements could include predictive analytics on ride demand, or integration with real-time booking data for live operational dashboards.

# Credits
Tutorial guidance and dataset sourced from: DataWolfs - Uber/Ola Power BI Project
