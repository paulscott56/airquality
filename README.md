# Air quality monitor

This is a simple python + influxDB + grafana based air quality monitor, using a Raspberry Pi Zero and the Rehau USB based air quality stick for indoor use. The code is based on an IBM Watson IoT project, found at https://www.ibm.com/blogs/internet-of-things/creating-home-glow-orb/

I have modified the Rehau USB code to not use IBM Watson as a broker endpoint, but to rather use a Dockerized (or not) InfluxDB data store for the time series data. I then use Grafana to create a dashboard to visualize the air quality data.

The dashboard for Grafana uses an InfluxDB data source called InfluxDB, and is the JSON document found in the repo. Simply import this data into your own grafana instance to use.

The airstick.py file is the python code that must run (as root) on the Raspberry Pi Zero. Please modify the IP address in the code to point to your own grafana server or instance. 
