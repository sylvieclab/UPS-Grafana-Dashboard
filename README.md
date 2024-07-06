# UPS-Grafana-Dashboard

![Image of the dashboard](https://github.com/sylvieclab/UPS-Grafana-Dashboard/blob/d0817126f004e498b0584d69536233e44b5c4183/UPS%20Dashboard.png?raw=true)

This is an initial implementation of a Grafana dashboard to monitor the UPS in my server rack. This utilizes the following containers:
- Network Utility Tools (NUT)
- nut-influxdbv2-exporter
- InfluxDB
- Telegraf
- and Grafana (obviously)

The dashboard utilizes a constant variable for the name of the bucket. If you import this dashboard, you will need to follow the instructins below to update the variable. This dashboard is likely to see changes as I continue to build upon and refine it.

Below are instructions and information I feel is useful to understand how the dashboard functions.

## Start Windows
Some of the panels have specific aggregate windows set, which means they will not change based on your window set in Grafana. A list of those panels are..
- Estimated Watts Last 24h
- Estimated Watts Last 7d
- Estimated Watts Last 30d
- Estimated Watts Last 60d

## Aggregate Windows
Some of the windows have aggregate windows set to reduce the amount of data points as I feel they are not necessary for granular tracking oft he specific statistic. Below is a list of those panels and what their windows is set to.
- Battery Charge History: 5 minutes
- Watts Used: 5 minutes


## Importing
When importing the dashboard, you will need to update the Constant Variable named "Bucket". This is the bucket in InfluxDB where you will pull from for your UPS information. This is completed after import by going to the gear icon in the top right, selecting "Variables" from the tabs menu, then clicking edit on the "Bucket" variable.
