# Santiago-Air-Pollution-Data

Welcome to the GitHub repository for the Santiago Air Pollution Data Dashboard. This dashboard provides insights into air pollution across the Santiago Metropolitan region using data from various monitoring stations.

## This is the github repo for Santiago air pollution data.

We collected hourly data from the Santiago Metropolitan Region (RM_data), which includes the following variables:

* `fecha`: Date in year-month-day format.

* `hora`: Hour of the day.

* `registros_validados`: Valid registered pollution value.

* `registros_preliminares`: Preliminary registered pollution value.

* `registros_no_validados`: Invalid registered pollution value.

* `contaminante`: Type of pollutant, which includes MP 10, MP 2.5, SO2, NO2, NOX, NO, CO, and O3.

* `estacion`: Monitoring station (`Cerrillos II`, `Cerrillos I`, `Cerro Navia`, `El Bosque`, `Independencia`, `La Florida`, `Las Condes`, `Pudahuel`, `Quilicura`, `Quilicura I`, `Parque O'Higgins`, and `Talagante`). Note that `Cerrillos II` and `Quilicura` only measure MP 10 and MP 2.5.

* `longitude` and `latitude`: Location coordinates of each monitoring station.

!!! Please keep in mind:

1. The available time periods for each pollutant vary across stations.

2. Most of the data are stored in `registros_validados`, but some are in `registros_preliminares` or `registros_no_validados`. The complete data set includes over 14 million observations.

Given the size of the hourly data set, Professor Stingone suggested reducing it by calculating the daily maximum value for each pollutant at each station. This reduced data set was used to build the dashboard for easier analysis.

## Using the Dashboard

You can run the dashboard by downloading this repository, opening the RM_Dashboard file in R, and clicking on `Run document`.

Here are three main part in this dashboard:

1. Station Map: Displays a static map of the 13 monitoring stations in the Santiago Metropolitan region, providing an overview of station locations.

2. Data Availability Heatmap: This section shows a heatmap of available data for each pollutant across stations over time, allowing users to easily see when data is available for each pollutant at each station.

3. Spatial-temporal Changes: This section offers an interactive visualization of the spatial-temporal changes in pollutant levels at the selected stations.

* Users can select specific monitoring stations and pollutants to explore. The left-hand side displays a time series line chart of the daily maximum levels of the chosen pollutant at the selected station.

* The right-hand side map shows the maximum pollutant values for all stations that have available data at a selected time point. Use the timeline slider to explore different time points. If no data is available for a given time point, the map will display a message indicating "No available data!"