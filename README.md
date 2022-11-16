# PyBer_Analysis


# **Purpose**
The purpose of this assignment was to perform an exploratory analysis on two CSV files between the date range of January to May 2019 using Python, Pandas, Jupyter Notebook, and Matplotlip for the company Pyber. The analysis should help PyBer determine how to allocate resources to cities by type, by creating charts that depict the relationship between:
- The type of city and the number of drivers and riders,
- The percentage of total fares, riders, and drivers by type of city
- The average fare per ride and fare per driver by city type
- The average fare per city type over the course of January to May 2019

### **Challenge Goal**
- Create a ride-sharing summary DataFrame by city type
- Create a multiple-line chart of total fares for each city type
- Analyze the PyBer data and summarize how the data differs by city type and how those differences can be used by decision-makers at PyBer

## **Resources**
- Resources: city_data.csv, ride_data.csv
- Code within:
- online lesson: PyBer.ipynb 
- challenge code: PyBer_Challenge.ipynb
- Software: Python, Pandas, Jupyter notebook, Matplotlib

### **Result**
In the online activity, I created a chart that showed the average fare versus the total number of rides. The bubbles in the chart were based on the average number of drivers for each city type: Urban, Suburban, and Rural. To create this chart I gathered the following information:
- The average fare for each type of city on the y-axis
- The total number of rides for each type of city on the x-axis
- Made the size of each marker, or bubble, correlate to the average number of drivers for each type of city
Based on the results, there are more rides in the Urban cities at a lower fare, while there are less rides in Rural cities at a higher fare.

![mean results](Fig1.png)

Next I pulled the information to create the summary statistics and to determine if there are any outliers by using a box-and-whisker plot. To display this chart I gathered the following information:
- Found the ride fares for each city
- Set the x_axis equal to ride fares for each city
The plot shows that the average number of drivers in Urban areas far exceeds the average number of drivers in Rural areas by around 9 times. The Suburban cities had significantly less average drivers too.

![mean results](Fig2.png)

I calculated the percentage of the overall fares for each type of city and depicted it in a pie chart.
To create this pie chart, I found the following information:
- Get the total fares for each city type.
- Get the total for all the fares for all the city types.
- Calculate the percentage of the total fares for each city type.
Based on the pie chart, Urban cities accounted for the largest portion of total fares at almost 63%. Suburban accounted for almost 31% and Rural almost 7%.

![mean results](Fig5.png)

I calculated the percentage of total rides for each type of city and depicted it in a pie chart.
To create this pie chart, I found the following information:
- Get the total number of rides for each city type.
- Get the total rides for all the city types.
- Calculate the percentage of the total rides for each city type.
Urban rides accounted for the most rides taken at 68% followed by Suburban at 26% and Rural at 5%.

![mean results](Fig6.png)

I calculated the percentage of the total drivers for each city type and depicted it in a pie chart.
To create this pie chart, I found the following information:
- Get the total number of drivers for each city type.
- Get the total drivers for all the city types.
- Calculate the percentage of the total drivers for each city type.
Urban drivers accounted for the most drivers at almost 81% followed by Suburban at 16.5% and Rural at almost 3%.

![mean results](Fig7.png)


For the challenge, I created a ride-sharing summary DataFrame by city type. To do this, I took these steps:
- The total number of rides for each city type was retrieved
- The total number of drivers for each city type was retrieved
​- The sum of the fares for each city type was retrieved
​- The average fare per ride for each city type was calculated
- The average fare per driver for each city type was calculated
- A PyBer summary DataFrame was created
The summary DataFrame showed that the city type, Rural, had the least amount of rides at 125 and only had 78 drivers. It accounted for the least amount of money at $4,327.93 but had the highest average fare per ride at $34.62 and the highest fare per driver at $55.49. So the driver fare cost more than the ride fare. The Urban city type had the most rides, 1625, and the most drivers, 2405. It made the most money overall, $39.854.38. However the urban cities average fare per ride was the least expensive at $24.54 and the driver’s fare was the least at $16.57. Suburban cities had 625 rides with 490 drivers and accounted for $19,356.33. The average fare per ride was $30.97 and the average fare per driver was $39.50.

![mean results](ride_sharing_summary.png)


The last step of the challenge was to create a multiple-line chart of total fares for each city type. To do this I followed these steps:
- A DataFrame was created using the groupby() function on the "type" and "date" columns, and the sum() method is applied on the "fare" column. 
- A DataFrame was created using the pivot() function where the index is the "date," the columns are the city "type," and the values are the "fare." 
- A DataFrame was created using the loc method on the date range: 2019-01-01 through 2019-04-28.
- A DataFrame was created using the resample() function in weekly bins and shows the sum of the fares for each week.
- The labeled line chart in created
The line chart shows that over the course of the year between January and May 2019, Urban city rides accounted for the most fares. Suburban fares accounted for second most and Rural fares accounted for the least. All cities had a peak in fares in the weeks just before march and the weeks just after March begins. However, right at the start of March, all cities experience a dip in overall fares. Overall, the weeks leading up to March and just after make up some of the highest fares for Urban cities.
![mean results](Total_Fare_by_City_Type.png)

### **Summary**
Based on the analysis to the two csv’s, the following recommendations can be made:
- provide three business recommendations to the CEO for addressing any disparities among the city types.
- Urban cities make up the majority of the revenue. Allocate more resources to Urban cities 
- Suburban cities make up the second most revenue. Allocate more resources to Suburban cities.
- Rural cities make the least amount of revenue and on average the fare to the driver is greater than the fare the rider pays so PyBer is losing money. Pull out of Rural areas to creat more focus on Suburban and Urban
By looking at the driver count data and fare data, can you get a sense of the overall revenue?
