# Detection of abnormal activity using a wearable biosensor

## Background:

This repository is an adaptation of a capstone project realised during a Data Science bootcamp. The dataset used here is WESAD, a publicly available dataset for wearable stress and affect detection available [here](https://archive.ics.uci.edu/ml/datasets/WESAD+%28Wearable+Stress+and+Affect+Detection%29). They published the following paper:
Philip Schmidt, Attila Reiss, Robert Duerichen, Claus Marberger and Kristof Van Laerhoven. 2018. Introducing WESAD, a multimodal dataset for Wearable Stress and Affect Detection. In 2018 International Conference on Multimodal Interaction (ICMI ’18), October 16–20, 2018, Boulder, CO, USA. ACM, New York, NY, USA, 9 pages. https://doi.org/10.1145/3242969.3242985

## Project Goals : Find patterns in the sensor signals that correlate with a stress status.

## Objectives :

This project focuses on analysing data derived from wearable sensors using the time series forecasting method Prophet from facebook.

The overall goal is to find patterns in the sensors' signals that correlate with a stress status.

Please note that as of July 2020, this project is under development and may contain bugs. Please contact me for any information.

## Milestones:
**Milestones 1**: Fetch and structure and normalize the data. Identify patterns, detect certain activities.

**Milestones 2**: Possibility to detect early change in stress data.

## Data:

Please find below a brief description from the [WESAD repository webpage](https://archive.ics.uci.edu/ml/datasets/WESAD+%28Wearable+Stress+and+Affect+Detection%29):

* Raw sensor data was recorded with two devices: a chest-worn device (RespiBAN) and a wrist-worn device (Empatica E4).
* The RespiBAN device provides the following sensor data: electrocardiogram (ECG), electrodermal activity (EDA), electromyogram (EMG), respiration, body temperature, and three-axis acceleration. All signals are sampled at 700 Hz.
* The Empatica E4 device provides the following sensor data: blood volume pulse (BVP, 64 Hz), electrodermal activity (EDA, 4 Hz), body temperature (4 Hz), and three-axis acceleration (32 Hz).

The [dataset's readme-file](wesad_readme.pdf) contains all further details with respect to the dataset structure, data format (RespiBAN device, Empatica E4 device, synchronised data), study protocol, and the self-report questionnaires.

## Approach
**Skills**: Time-series analysis of data.

**Output**: Analysis report of activity. Dashboard for a patient-specific overview

**Value Proposition**: Tells the medical staff any stress-related physiological change.

**Integration**: Dashboard accessible through a web interface to be developed on Streamlit

**Customers**: Medical staff

**Cost**: Written acknowldegement.

**Revenue**: Stress detection may lower medical cost by enabling early detection of stress-related health issues. 

### Code structure

**`1_exploration`**: first handling of the data. Plotting time-series to find the relevant duration and amplitude of patterns. Data interpretation on a few examples.

**`2_forecasting`**: Anomaly detection using time-series forecasting using Prophet from facebook

**`3_dashboard`**:  Web interface dedicated to the caregivers to inform and alert on the patient activities.

> Questions:
> Contact Guillaume Azarias at guillaume.azarias@hotmail.com
