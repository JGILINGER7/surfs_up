# Surfs Up Analysis 

## Overview
### Goal 
    Using SQLITE and Python we looked at weather data to anaylyze variables that could effect the sales of a surf/ice cream shop on Awahoo. This analyiss focused on temperature and percipitation the two most significant weather factors on the island.

## Results
   Although the temperature data shows the June to December differences to be minimal by the standards of most of the world, the expecations of Hawaii are for ideal weather meaning three key points determine the difference. 
   *Average temperature in December is almost 4 degrees lower than in June
   *The minimum temperature in December is 56 degrees compared to June's 64. 
   *The median temperature in December is only 4 degrees cooler than June's median of 75
## Summary
    Taking this data into account we can expect some lower sales days in December. But overall we can still expect most days in the month to be ideal for ice cream and or surfing. To bolster this data I ran two additional queries.  The first is to look at rainfall for December as a month of low temperatures and high rainfall could be costly to the business. The second is to be able to access the summary statistics for the entire year to see if December and June line up with trends across the entirety of the year. Although generally June and December represent opposite polls of weather it is important to have a more certain basis to look at the data from. 

### Query 1  
   '''
   dec_rain = session.query(Measurement.date, Measurement.prcp).\
    filter(func.strftime("%m", Measurement.date) == "12").all()
   '''
### Query 2 
    '''
    temp_data = session.query(Measurement.date, Measurement.tobs).all()
    '''
 