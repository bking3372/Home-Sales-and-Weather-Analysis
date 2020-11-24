# An Analysis of the Relationship between Home Sales and Weather Patterns

This was a team effort with the following members:  Katie Harris, Betsy King, Wenbo Sun, James Shin

## Objective:  Determine if there are relationships between home sales across the country and specific weather patterns, including temperature, humidity levels, amount of precipitation, and amount of cloud cover.

### Data:

The data for the analsyis was collected from the following sources:
* Home sales from Zillow for over 20,000 US cities; this was narrowed to the top 1,000 most populous cities in the US.  The Zillow data was aggregated to 3 years of monthly data for 2017-2019.
* Weather data from the Visual Crossing API; this data was also at a monthly level for the three year period 2017 to 2019.
* The cities were grouped into regions based on the four primary US Census regions:  Northeast, Midwest, South and West.

Cleaning the data brought the total number of cities to 922:
*  The Zillow data did not include home sales information for all of the top 1,000 most populous US cities.
*  Some cities did not have a full three years of data (either home sales or weather information) in the 2017 to 2019 time period and were eliminated.



### Analysis and Conclusions:

The data was analyzed by looking at correlations between home sales and weather patterns by month and fitting linear regression models.

**It was concluded that there are relationships between home sales across the country and different weather patterns.**

* Across all four regions, home sales are higher when temperatures are higher (i.e., in the summer months).  Temperature has the strongest relationship with home sales and has an impact on trends seen with the other weather variables.

  **Correlation of Home Sales & Temperature:**
    - Northeast:  0.85
    - Midwest:    0.91
    - South:      0.78
    - West:       0.82


   **Linear Regression Models by Region:**
   
     ![NETemp](https://github.com/bking3372/Home-Sales-and-Weather-Analysis/blob/master/Images/NE_Temp_Sales.png)
     ![MWTemp](https://github.com/bking3372/Home-Sales-and-Weather-Analysis/blob/master/Images/MW_Temp_Sales.png)
     ![SOTemp](https://github.com/bking3372/Home-Sales-and-Weather-Analysis/blob/master/Images/SO_Temp_Sales.png)
     ![WETemp](https://github.com/bking3372/Home-Sales-and-Weather-Analysis/blob/master/Images/WE_Temp_Sales.png)

* The relationship between home sales and humidity level differs by region:
  -  In the West, home sales are higher when humidity is lower since the summer months tend to have lower humidity levels.  The same relationship also exists in the Midwest.
  -  In the South, humidity does not vary a lot during the year so humidity levels are not related to home sales.
  -  In the Northeast, home sales are actually higher when humidity is higher but the relationship is fairly weak.

* Home sales are higher when precipitation is higher for most regions (Northeast, Midwest, South) as the amount of precipitation is higher in the summer months, when home sales are higher.
  -  The exception is the West region which has low precipitation levels in the summer months.

* Home sales are higher when cloud cover is lower as it tends to be sunnier in the summer months; the relationship is stronger in some regions and weaker in others.

