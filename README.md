# MiTra Data 

This repository contains Python scripts for processing and visualizing MiTra traffic trajectory data. 

### Data download:
MiTra data can be downloaded from https://doi.org/10.25532/OPARA-706


### Data Format
To access the trajectory data, navigate to the Data_T* folder of the desired flight campaign, e.g., (Data_T1) to access the trajectory CSV files. 
Each CSV file contains trajectory data for individual vehicles, including timestamps, vehicle IDs, and position coordinates.

The input trajectory data should be in CSV format and contain the following columns:

|Column Name | Description |
| --- | --- |
|Vehicle_ID | Unique Vehicle ID for given flight campaign (and drone in case of single drone data) |
|Vehicle_type | Type of Vehicle |
| Time [s] | Current timestamp |
| x [m] | UTM Coordinates longitude at the current time |
| y [m] | UTM Coordinates latitude at the current time |
|Speed [km/h]|Speed at the current time|
|Lon. Acc. [ms-2]|Longitudinal Acceleration at the current time in m/s² (a positive value means acceleration and a negative value means deceleration)|
|Lat. Acc. [ms-2]|Lateral Acceleration at the current time in m/s² (a positive value means acceleration to the right, and a negative value means acceleration to the left)|
|Angle [rad]|Heading angle|
|Vehicle_length [m]|Length of vehicle (Average for given type)|
|Vehicle_width [m]|Width of vehicle|



### Working with the data
The analysis includes calculating distances traveled by vehicles, identifying the vehicle with the maximum distance traveled, and fitting a linear regression model to estimate the trajectory angle.


### License
This project is open-source and available under the MIT License.

