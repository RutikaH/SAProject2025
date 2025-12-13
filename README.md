# Dynamic Pricing for Urban Parking Lots

## Overview
Implemented a dynamic pricing system for urban parking lots that adapts prices
using real-time demand signals, feature engineering, and competitive pricing
logic. The system focuses on interpretable models, real-time aggregation, and
business-aware constraints to improve utilization and pricing stability.

## Problem Statement
Static parking prices do not reflect real-world demand, leading to peak-hour
congestion, off-peak underutilization, and inefficient pricing. This project
demonstrates how data-driven pricing can address these challenges.

## Tech Stack
- Python 3: Core implementation
- Google Colab: Execution environment
- Pandas, NumPy: Data preprocessing and feature engineering
- Matplotlib: Exploratory analysis
- Bokeh: Interactive visualization
- Pathway: Real-time streaming and window aggregation
- GitHub: Version control

## System Workflow

### Data Preprocessing
- Cleaned parking data and encoded categorical variables.
- Converted and sorted time fields for window-based aggregation.

### Feature Engineering
- Occupancy rate, queue length, and traffic intensity.
- Rolling averages for demand smoothing.
- Geo-proximity score, special day, and vehicle type indicators.

### Real-Time Aggregation
- Hourly tumbling windows using Pathway.
- Computation of peak and average demand metrics.

### Pricing Models
- **Model 1 (Baseline):** Linear pricing based on occupancy and queue length.
- **Model 2 (Advanced):** Weighted pricing using all engineered features,
  designed for smoother and demand-aware price behavior.

### Competitive Pricing
- Prices normalized and bounded for stability.
- Competitor prices simulated (±10%).
- Competitive logic applied to maintain market alignment.

### Visualization
- Interactive comparison of baseline, advanced, competitor,
  and final prices over time.

## Key Outcomes
- Improved utilization balance compared to static pricing.
- Better handling of demand spikes with controlled volatility.
- Market-aware pricing through competitive simulation.

## Assumptions
- Hourly aggregation chosen based on common industry practices.
- Certain parameters are assumed and tunable.
- Competitor pricing is simulated due to data limitations.

## Project Structure
- `saproject_final.ipynb`: Analysis, feature engineering, pricing logic.
- `dataset.csv`: Parking and traffic data.
- `diagram.png`: System architecture.


