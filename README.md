# weather_events
Analysis of historic weather events from NOAA since 1996

Initial repo with states_shape.zip, 50 states shapefile neccessary for geopandas mapping, storm_events.zip, csv file of the historic weather events from NOAA since 1996, and analysis of those events in StormEventsAnalysis.ipynb.
Jupiter Notebook, py 3.10.12, numpy, pandas,matplotlib, geopandas, and statsmodels.api

**Overview**
In this analysis, I investigated historical storm data from the National Centers for Environmental Information from NOAA. The Storm Events Database covers the time period between January 1950 to September 2023, at this time. The database was created to document significant weather phenomena with damage to people, property or commerce, unusual weather events, and significant meteorlogical events. The csv of the Storm Events Database can be found at https://www.ncei.noaa.gov/pub/data/swdi/stormevents/csvfiles/. For the purposes of this analysis, I have chosen to focus on the Storm Events Details published December 17, 2023 (StormEvents_details-ftp_v1.0_d2023_c20231217.csv.gz)

The event types collected have changed over time. During the period from 1950 to 1955, data was collected on tornados. From 1955 to January 1996, event data was collected for Tornado, Thunderstorm, Wind, and Hail events. From January 1996 to September 2023, event data was collected on 48 event types as detailed by the National Weather Service in instruction 10-1605 (https://www.nws.noaa.gov/directives/sym/pd01016005curr.pdf)

**Data Set**
The weather event dataset includes 1,630,114 unique entries of weather significant weather events from January 1996 to September 2023. It is organized by Episode and Event, where an episode may be comprised of several meoterological events with unique event types, while still belonging to the same primary meteorological episode. It includes columns for:

  
  - Event and episode identifiers - with a unique event id and a shared episode id for grouping episodes of connected events. For instance a low pressure storm episode may have several events that include wind, hail, and flash flooding
  - Event date/time with beginning and ending year and month, day, and time, and a column for a combined datetime each for beginning and ending
  - Event location with State, State id, regional type (county, parish, etc), regional id, and regional name, event beginning and ending locations, beginning and ending latitude and longitude, and beginning/ending azimuth directions
  - Event scale details for tornados including scale, length, width, magnitude type, flood_cause
  - Event impact with columns for injuries direct and indirect, deaths direct and indirect,  and monetary property damage, and crop damage
  - Data source
  - Episode and Event narrative descriptions of the event

**Exploratory Questions**
Weather event frequency over time:
- How many extreme weather events occur in a year?
- Are extreme weather events occuring more frequently?
- What does the frequency of weather events look like in each state over time?
- What is the most frequent event type by year?
Cost of Weather Events:
- When looking at cost to property or crops, which weather events are most costly?
- Which states have the highest weather related cost burden?


