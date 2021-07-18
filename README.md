# PyBer_Analysis

## Overview of PyBer Ride-Sharing Analysis
PyBer is a ride-sharing app company. 
Python scripts are required to analyze the relationship between city types, the number of drivers, the number of riders and the total fares.
PyBer executives require data visualizations that will display the analysis results in an easy-to-understand table and graph.  
This will allow them to make decisions on how to improve access to ride-sharing services and determine the affordability of underserved city types.

### Purpose
This analysis summarizes how ride-sharing data differs by city type.
The three city types are: rural, suburban and urban.
The Python script [PyBer_Challenge.ipynb](PyBer_Challenge.ipynb) is written in a Jupyter Notebook that utilizes the Pandas Library and MatPlotLib.

## PyBer Ride-Sharing Results
The city and ride data for this analysis was imported from [city_data.csv](Resources/city_data.csv) and [ride_data.csv](Resources/ride_data.csv).
To begin the analysis the data from these files was merged into one summary DataFrame.
With the summary DataFrame a DataSeries was created for the total rides by city type, the total drives by city type and the total amount of fares for each city type.
To generate the total rides by city type the groupby function was used in this code 'ride_total_city_type = pyber_data_df.groupby('type')["ride_id"].count()'.
The code was refactored for the total drivers for each city type and the total fares by city type.

### Differences in Ride-Sharing Data by City Type:
- Rural
	- The total number of rides was 125 and the total drivers was 78. 
	- The total fares was $4,327.93.
	- The average fare per ride was $34.62 and the average fare per driver was $55.49. 
	
The rural population is smaller and often requires rides that are a greater distance.
Due to this it has the fewest drivers and number of rides.
Although the demand for ride-sharing is low the average fare per ride and driver is the highest of the different city types.
 
- Suburban
	- The total number of rides was 625 and the total drivers was 900. 
	- The total fares was $19,356.33.
	- The average fare per ride was $30.97 and the average fare per driver was $39.50. 

The suburban city type accounts for approximately 30% of the total fares at PyBer and 26% of the total rides.	
The average fare per ride and average fare per drive is higher than in urban cities and lower than rural areas.	
		
- Urban
	- The total number of rides was 1,625 and the total drivers was 2,405. 
	- The total fares was $39,854.38.
	- The average fare per ride was $24.53 and the average fare per driver was $16.57.

Urban cities account for PyBer's largest number of drivers, rides and fares.
They account for a significant portion of business.
Based on having the lowest average fare per ride and average fare per driver it is reasonable to conclude that the service is more affordable.

This data is summarized in a table in [PyBer_Challenge.ipynb](PyBer_Challenge.ipynb).
A multiple-line chart [Pyber_fare_summary.png](Analysis/Pyber_fare_summary.png) displays the total fares for each city type for the time period between January 1, 2019 to April 4, 2019.
To create the multiple-line chart that shows the total weekly fares for each city type required the use of the groupby, pivot, loc and resample functions.

## PyBer Summary

### Three Business Recommendations
The urban city type generates the most revenue for PyBer with approximately 63% of the total fares.
It is critical to focus marketing resources to urban areas and ensure it is properly staffed to meet higher customer demand.
There is a need for PyBer's ride-sharing services in rural and suburban markets.
With less demand in these areas the average fare price for each ride is higher. 
To effectively support growth in these areas requires a customized strategy.
Providing discounts for scheduling in advance could lower customer costs and help PyBer utilize drivers in the most effective manner.
Overall a loyalty program could increase the demand for PyBer's services as well as provide additional customer data for future analyses. 


