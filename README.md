DYNAMIC PRICING FOR URBAN PARKING LOTS


Overview

This project's objective is to implement a dynamic pricing system for urban parking lots using real-time data and feature engineering. The ultimate goal is to optimize pricing strategies and parking prices based on demand signals, appropriate features, ensuring both technical and business requirements, and simulated competitive pricing. 

TECH STACK
Google Colab  : execution environment
Python 3      : core programming language
Pandas, Numpy : for data processing and feature engineering
Matplot       : for visualizing and understanding data
Pathway       : for real-time data streaming and processing,for real-time window aggregation
bokeh         : for interactive data visualization
GitHub        : collaboration and version control

Architecture Flow

Data Ingestion and pre-processing:
parking data is loaded and preprocessed.
some categorical columns are converted to numerical columns.
time columns are converted to datetime and sorted for windowing.

Feature engineering:
necessary features are added and sorted main key features are rolling average of occupancy rate,competitor prices and geo proximity score.

Pathway(real-time aggregation):
data is aggregated into hourly tumbling windows as suggested from industrial practices, for each window necessary peak and average values are calculated.

Demand score and price calculation:
Model 1: Baseline price using occupancy and queue length.
Model 2: Advanced price using all engineered features in a weighted sum.
Prices are calculated in Pathway, then exported for further processing.

Post-Processing 
Prices are normalized and clipped to business-appropriate bounds.
Simulated competitor prices are generated (±10% of Model 2 price).
Competitive pricing logic is applied (undercut competitor if needed).

Visualization 
Interactive plots show Model 1, Model 2, competitor, and final competitive prices over time.
 



Feature Summary
Occupancy Rate: Shows how full the lot is—higher rates mean higher prices.
Queue Length: Longer lines signal more demand, raising prices.
Traffic Nearby: More traffic means more people looking for parking.
Special Day Indicator: Prices go up during events or holidays.
Rolling Average of Occupancy: Smooths out sudden changes for steadier pricing.
Geo Proximity Score: Lots closer to the city center get higher prices.
Vehicle Type: Prices adjust for different vehicle categories.
Simulated Competitor Price: Mimics real market competition to keep our prices competitive.


