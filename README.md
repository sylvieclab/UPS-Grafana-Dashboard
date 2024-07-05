# UPS-Grafana-Dashboard

![Image of the dashboard](https://github.com/sylvieclab/UPS-Grafana-Dashboard/blob/d0817126f004e498b0584d69536233e44b5c4183/UPS%20Dashboard.png?raw=true)

This is an initial implementation of a Grafana dashboard to monitor the UPS in my server rack. This utilizes the following containers:
- NUT (Network Utility Tools)
- InfluxDB
- Telegraf
- and Grafana (obviously)

The dashboard utilizes a constant variable for the name of the bucket. If you import this dashboard, you will need to follow the instructins below to update the variable. This dashboard is likely to see changes as I continue to build upon and refine it.

# Instructions:

When importing the dashboard, you will need to update the Constant Variable named "Bucket". This is the bucket in InfluxDB where you will pull from for your UPS information. This is completed after import by going to the gear icon in the top right, selecting "Variables" from the tabs menu, then clicking edit on the "Bucket" variable.
