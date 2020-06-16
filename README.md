# Identification of abnormal activity from time series

## Background:

XXXX is a voice-first solution that fosters autonomy and safety in the everyday life of elderly people. Users can communicate with relatives and call for help. In addition activity patterns can be derived from different sensors like CO2, temperature, noise, etc. If irregularities in the data are detected, CARU actively notifies caregivers.

## Project Goals : Find patterns in the sensor signals that correlate with a person's activity.

## Objectives :

This project focuses on analysing data derived from sensors deployed in households.

The overall goal is to find patterns in the sensors' signals that correlate with a person's activity.

## Milestones:
**Milestones 1**: Normalize the data, identify patterns, detect certain activities.

**Milestones 2**: Real-time activity reporting every 15 - 30 minutes. Be able to detect an activity (and maybe the type of activity) and send a notification.

## Data:
The data for this project contains anonymized time series data sampled every 20 seconds. You will know which night belongs to a given person, and each person will have at least 14 nights recorded. The type of residence is known, but not whether the device is placed in a bedroom or living room.
Examples are the times someone goes to bed or wakes up in the morning, or nightly bathroom breaks. Patterns may also include unknown activities that nevertheless occur regularly across nights and persons. Create an activity report after each night.

* device = one Caru device; always one per resident. However the tenant may
 move the device between rooms/residents.
* tenant = the institution that bought the devices. They distribute them to their rooms/residents.
* ts_date: Date and time. Datetime format. [UTC]
* light: Instantaneous clear light [counts] 
* temperature: Instantaneous temperature [°C]
* humidity: Instantaneous relative humidity [%]
* co2: Instantaneous CO2 [ppm]

* *Room types*:
    * See TenantRoomOverview.pdf (ind data)
    * Some rooms are unoccupied for the entire time frame given
    * Some rooms are occupied for the entire time frame given
    * Some rooms had residents move in/out in the time frame given (i.e. first
nobody lived in the room for a few days/weeks, and then somebody started living in the room. Or vice versa.)
* Sometimes chunks of data are missing, e.g. when the tenant unplugged the devices (for unknown reasons)

### Approach
**Skills**: Time-series analysis of data. Clustering - pattern analysis

**Output**: Analysis report of activity. Dashboard for a patient-specific overview

**Value Proposition**: Tells the caregiver/family if a resident is behaving normally or exhibit an abnormal activity. Detects persons in need of help

**Integration**: Dashboard accessible through a web interface

**Customers**: Caru's customers

**Cost**: Free from the Propulsion Academy

**Revenue**: Increase efficiency of caretakers

### Code structure

**`1_exploration`**: first handling of the data. Plotting time-series to find the relevant duration and amplitude of patterns. Data interpretation on a few examples.

**`2_between-day_clustering`**:  k-shape using Dynamic Time Warping and hierarchical clustering

**`3_within-day_clustering`**:  

**`4_forecasting`**: Anomaly detection using time-series forecasting using Prophet from facebook

**`5_dashboard`**:  Web interface dedicated to the caregivers to inform and alert on the patient activities.
