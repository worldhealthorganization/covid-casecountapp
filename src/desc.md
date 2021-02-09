# Interacting With This App

This app allows you to visually explore the trajectory of COVID-19 case and death counts according to several data sources at different geographic resolutions. Each geographic entity has several metrics associated with it which you can use to sort, filter, and page through visualizations to get a feel for the state of the pandemic.

Click the blue folder icon in the top left to select different geographic resolutions to view (e.g. global, WHO regions, countries). Click the icons in the left sidebar to gain access to several controls such as arranging the grid layout, choosing what metrics to show as labels beneath each plot, filter, sort, and choose pre-defined views of the visualizations.

Click the question mark icon in the top right corner of this app for more information about the interactive controls.

# Data Sources

The numbers reported represent the latest data from each source.

# Update Frequency

WHO, John Hopins and Worldometer providing daily data. ECDC is providing weekly data (since 17 Decemeber 2020, daily data up to 14 December 2020). 

Handling of weekly data on charts showing data by day: Weekly data will be distributed as evenly as possible over the 7 days of the week. On charts showing data by day. 


## WHO

- **Source**: Direct database connection to data as reported here: https://www.who.int/emergencies/diseases/novel-coronavirus-2019/situation-reports/
- **Update frequency**: A full time series is provided for each geographic entity and variable. Updates are made to the database between 1 and 20 times a day. Major updates occur about once or twice a day, and typically occur between 14:00 and 16:00 UTC.
- **Day binning**: What time zone is used to constitute a day for this data is unknown. Due to the fact that the numbers are reported post-binning, we are not able to adjust the time binning.

## Johns Hopkins CSSE (JHU)

- **Source**: csv files stored on GitHub: https://github.com/CSSEGISandData/COVID-19
- **Update frequency**: A full time series is provided for each geographic entity and variable, updated daily at 12am PDT. The timeliness of JHU updates is typically a day behind the other sources.
- **Day binning**: Case and death counts are binned into days defined by UTC time. Due to the fact that the numbers are reported post-binning, we are not able to adjust the time binning.


## Worldometer (WOM)

- **Source**: Web scraping tables published here: https://www.worldometers.info/coronavirus/
- **Update frequency**: Counts are updated very frequently - usually at least more than once every 5 minutes.
- **Day binning**: We bin counts by day according to UTC time. Since we are constantly scraping this data, it is possible to bin in other ways.

## ECDC

- **Source**: Pulled from opendata.ecdc.europa.eu. URL: https://opendata.ecdc.europa.eu/covid19/casedistribution/csv
- **Update frequency**: ECDC switched to a weekly reporting schedule for the COVID-19 situation worldwide and in the EU/EEA and the UK on 17 December 2020. Hence, all daily updates have been discontinued from 14 December. ECDC will publish updates on the number of cases and deaths reported worldwide and aggregated by week every Thursday.
- **Day binning**: Case and death counts are binned into weeks.

# Available Metrics

A full listing of metrics and their descriptions is provided at the bottom of this document. Some of them warrant further explanation.

Metrics that start with `cur_` correspond to latest day's total counts or deaths. Metrics that start with `prev_` correspond to the total counts of the previous day.
