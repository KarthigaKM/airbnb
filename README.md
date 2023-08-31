# [ PROJECT : Airbnb Analysis](https://github.com/KarthigaKM/airbnb)
## overview
 * This repository contains a comprehensive Airbnb Data Analysis Dashboard, which is built to provide insights into Airbnb listings data sourced from a MongoDB database. 
 * The dashboard offers various interactive visualizations and filters to allow users to delve deeper into specific aspects of the data.
## Features
 * Geospatial Visualization: Map-based visualization of Airbnb listings with price as the color indicator.
 * Price Analysis and Visualization: Analyze average prices based on property types, months, and suburbs.
 * Availability Analysis by Season: Visualize the average availability of Airbnb listings across different seasons.
 * Location-Based Insights: Scatter map visualization to highlight average prices in different neighborhoods.
 * Filter Options: The sidebar includes options to filter the visualizations based on property type, neighborhood, and date range.
## Dependencies
 * pymongo: For interfacing with MongoDB.
 * pandas: For data manipulation and analysis.
 * matplotlib & seaborn: For plotting static visualizations.
 * plotly: For interactive visualizations.
 * streamlit: For creating the web-based dashboard.
 * bson.decimal128: To handle MongoDB's Decimal128 datatype.

# Airbnb Data Analysis

This repository contains various data visualization and analysis functions tailored for Airbnb datasets. The primary focus is on visualizing price-related insights and understanding property availability patterns.

## Functions:

### 1. `plot_map_with_price(df)`
![](https://github.com/KarthigaKM/airbnb/blob/main/pic/geovisual1.png)
**Description:** This function visualizes property prices on a geographical map. It takes a DataFrame containing latitude, longitude, and price data.

- Cleans the 'price' column by converting it to a numeric column and removing non-numeric characters.
- Fills missing values in the 'price' column with the median.
- Plots a scatter map with the 'price' as the color indicator.

### 2. `plot_avg_price_by_property_type(df)`
![](https://github.com/KarthigaKM/airbnb/blob/main/pic/barplot.png)
**Description:** This function visualizes the average property prices based on property types.

- Converts the 'last_review' column to a datetime format.
- Calculates the average price by property type.
- Plots an interactive bar chart of average price by property type.

### 3. `plot_avg_price_by_month(df)`
![](https://github.com/KarthigaKM/airbnb/blob/main/pic/piechart.png)
**Description:** This function shows a pie chart depicting the average property prices across different months.

- Extracts the month from the 'last_review' column.
- Calculates the average price by month.
- Plots an interactive pie chart of average price by month.

### 4. `plot_avg_price_by_suburb(df)`
![](https://github.com/KarthigaKM/airbnb/blob/main/pic/barplot2.png)
**Description:** This function visualizes the average property prices in various suburbs.

- Extracts the suburb from the 'address' column.
- Calculates the average price by suburb.
- Plots an interactive bar chart of average price by suburb.

### 5. `plot_correlation_heatmap(df, exclude_columns=[], vmin=-1, vmax=1)`

**Description:** This function generates a heatmap to visualize the correlation between numeric columns in the dataset.

- Computes the correlation matrix for the provided DataFrame.
- Visualizes the correlation matrix using a heatmap.

### 6. `plot_boxplots_for_outliers(df, columns_to_check=['price', 'weekly_price', 'monthly_price'])`

**Description:** This function creates box plots for specified columns to visually check for outliers.

### 7. `plot_seasonal_availability(df)`
![](https://github.com/KarthigaKM/airbnb/blob/main/pic/seasonanl.png)
**Description:** This function visualizes the seasonal availability of Airbnb listings.

- Extracts availability data for different periods.
- Defines seasons based on Northern Hemisphere.
- Calculates average availability for each season.
- Visualizes the seasonal availability using a bar chart.

### 8. `generate_map_by_neighborhood_avg_price(collection)`
![](https://github.com/KarthigaKM/airbnb/blob/main/pic/newplot%20(3).png)
**Description:** This function generates a scatter map based on average price by listing location for each neighborhood.

- Uses a MongoDB collection containing the listings data.
- Aggregates data to find average prices by neighborhood.
- Visualizes the average prices on a scatter map.




