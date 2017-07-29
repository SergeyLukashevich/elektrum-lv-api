# Library and application to get electric meters measures from 'elektrum.lv' site

Disclaimer: This library and application, have no any connection neither with 'elektrum.lv' site creators nor 'AS Latvenergo'.
Also, the data you get are mirrored from a site, and just how they are. Mainly, it's just a web site parser 
and realization of my idea.  

## Precondition:
- Registration for 'elektrum.lv'. If you are not a Latvian resident, most likely this application won't be useful for you. 

## Use cases:

### InfluxDB

Main idea of this project is to monitor electric meters data,
add analytics, reports and visualize it. For this purposes very suits
combination of InfluxDB and Grafana. If you wish is possible to add alarms into
Grafana for monitoring your consumption limits. But take into account that source data on a site doesn't provided in real-time.

![Grafana screenshot](/doc/Capture.png?raw=true)

### CSV

You can just export data into CSV file in format `date;kWh`

## Library:
    TODO

## Application:
- Download 'TODO.jar'
- Place 'settings.yml' near the jar file.
- Set your credential for elektrum.lv site.
- If you plan to use export into InfluxDB, setup respective section settings. For export into CSV, it's not necessary.

### Command line examples 
 - `java -jar TODO.jar csv --period month -o output.csv --debug 2017-01`
 
    Exports data summed by month into CSV file from 1 January 2017 till now
 - `java -jar TODO.jar csv --period day -o output.csv --info 2016 2017`
 
    Exports data summed by day into CSV file from 1 January 2016 till 31 December 2017
 - `java -jar TODO.jar influxdb --period year --info 2016 2017`
 
    Exports data into InfluxDB from 1 January 2016 till 31 December 2017
 - `java -jar TODO.jar influxdb --period day --increment`
 
    Exports data into InfluxDB only recent data. Note that `--increment` option works with `influxdb` only
 