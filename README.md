# econ-final-project-ML-prediction

1. Research and Prediction Question 
Did the implementation of congestion pricing policies in New York City on January 5, 2025, reduce the number of 2-axle passenger cars entering Manhattan's Congestion Relief Zone (CRZ) compared to 2-axle passenger cars entering Greater Manhattan? (Greater Manhattan: area in Manhattan outside of the CRZ) 

2. Dataset and Source 
Dataset: MTA Bridges and Tunnels Hourly Crossings: Beginning 2019
Source: New York State Open Data, Metropolitan Transportation Authority (MTA)
https://data.ny.gov/Transportation/MTA-Bridges-and-Tunnels-Hourly-Crossings-Beginni/ebfx-2m7v

Filtered to only include the following: 
2-axle passenger cars 
Dates between January 1, 2024, and February 1, 2026 (1 year before and after congestion pricing was in effect) 
Queens Midtown Tunnel, Hugh L. Carey Tunnel, Henry Hudson Bridge (bridges removed from the dataset did not provide access to either the CRZ or Greater Manhattan) 

The hourly data intervals were aggregated into daily totals. 

Treatment group: Queens Midtown Tunnel, Hugh L. Carey Tunnel, which directly feed into the CRZ
Control group: Henry Hudson Bridge, enters Greater Manhattan

The dependent variable is the number of passenger cars entering Manhattan through each crossing per day. Other variables of interest: facility, day of the week, and whether congestion pricing was in effect. 

3. Stakeholder 
The Metropolitan Transportation Authority, a public authority, manages a transportation network that includes areas around New York City, Long Island, Southeastern New York State, and Connecticut. Understanding the impact of congestion pricing on traffic volumes is important for lawmakers, who want to understand the effectiveness of their policies. 

4. Models 
Model 1: Differences-in-Differences Regression 
The DiD model helps compare changes in daily 2-axle passenger car traffic going into the CRZ with changes in traffic going into Greater Manhattan before and after January 5, 2025. The regression will include controls for the day of the week, facility, and whether congestion pricing was in effect. An analysis of pre-policy trends between the two areas will evaluate the parallel trends assumption of DiD. 

Model 2: Random Forest Regression 
A random forest regression model helps to predict daily 2-axle passenger car traffic by using information about the facility, day of the week, and whether congestion pricing was in effect. I will compare the fit of the model and predictive performance to a linear regression, looking at RMSE, MAE, and R^2. 
