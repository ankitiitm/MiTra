# MiTra Data 

This repository contains Python scripts for processing and visualizing MiTra traffic trajectory data. 

### Data Overview
This dataset comprises original videos, tracking logs to validate the videos, and extracted trajectory data of naturalistic traffic collected using unmanned aerial vehicles (drones) over a 900-meter section of the A50 urban freeway in Milan, Italy. Nine flight campaigns, totaling 135 minutes, were conducted using six drones flying in a line to capture comprehensive coverage across all traffic states, from free flow to congested traffic. 
The dataset offers detailed trajectory data extracted from single drone videos (54 datasets from nine flight campaigns of six drones) and nine datasets of stitched footage from all six drones. With a granularity of 30 frames per second, we extracted over 100,000 vehicle trajectories from single drone videos and over 24,000 trajectories from stitched footage, enabling complete tracking of vehicles across five distinct categories: Cars (73.0%), Medium Vehicles (13.4%), Heavy Vehicles (11.3%), Buses (0.2%), and Motorcycles (2.1%). 
In addition to trajectory data, this dataset includes accompanying original videos and tracking files, showcasing the recorded traffic scenes, providing visual context, and enhancing the usability and interpretability of the trajectory data. The tracking file can be used to map the vehicle ID on the video, enabling various analyses as detailed in the user guide.
This dataset facilitates the analysis of driving behavior, traffic dynamics, and vehicle interactions, offering valuable insights for research, planning, and policymaking in transportation and urban mobility.


### Data download:
MiTra data can be downloaded from OPARA repository at https://doi.org/10.25532/OPARA-706


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
The given Python notebook (MiTra_plots.ipynb) gives a sample example of working with MiTra data. 
It includes calculating distances traveled by vehicles, identifying the vehicle with the maximum distance traveled, and fitting a linear regression model to estimate the trajectory angle.
Then, rotating the dataset parallel to the x-axis for better visualization and plotting the top view plot.


### License
This project is open-source and available under the MIT License.

