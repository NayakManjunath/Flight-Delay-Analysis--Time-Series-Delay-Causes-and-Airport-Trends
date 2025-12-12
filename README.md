### 📌 Flight Delay Analysis — Time Series, Delay Causes, and Airport Trends

This project analyzes U.S. airport-level monthly flight delay statistics using the BTS-style aggregated dataset that includes airline, airport, delay type, and time-based metrics. The notebook performs univariate, bivariate, and time-series EDA to identify patterns in on-time performance, major delay causes, and airport-level behavior.

### 🔍 Project Goals

The analysis focuses on understanding:

Monthly arrival delay behavior across airports

Percent of flights that arrive on time (delay ≤ 15 min)

Delay contribution by cause (carrier, weather, NAS, security, late aircraft)

Airport-wise delay performance and congestion patterns

Year-over-year trends and seasonal insights

Correlation between different delay causes

The project generates clean visuals to help airline analysts and airport planners identify bottlenecks and performance trends.

### 📁 Dataset Overview

The dataset includes columns such as:

FlightDate

UniqueCarrier

Origin

arr_flights

arr_delay, arr_delay_min

carrier_delay, weather_delay, nas_delay, security_delay, late_aircraft_delay

These fields represent aggregated monthly delay statistics per airline-airport combination.

### 🧹 Data Cleaning & Normalization

The notebook:

Strips whitespace from object columns

Converts delay fields to numeric

Creates monthly timestamps from FlightDate

Normalizes arrival delay to arr_delay_min

Computes cancellation rate and disruption metrics:

cancel_rate

weather_disruption_rate

carrier_disruption_rate

### 📊 Key Visualizations
-> Univariate Analysis

-> Distribution of arrival delays

-> Weather, NAS, carrier, security, and late aircraft delay histograms

-> Overall cancellation rate

-> Bivariate Analysis

-> Median delay by airline

-> Airport-level median arrival delays

-> Time-Series Analysis

### Includes:

-> Monthly % on-time arrivals

-> Monthly median arrival delay

-> Monthly weather delay trend

-> Top airports monthly on-time trend

-> Seasonal heatmaps

-> Rolling-average delay smoothing

-> Advanced Delay Cause Analysis

-> Total delay minutes by cause

-> Percentage share of delay causes

-> Stacked bar & stacked area charts

-> Year-over-year comparison by cause

-> Top airports for each delay type

-> Heatmap of delay cause intensity

-> Correlation matrix of delay types

All visualizations are saved inside the artifacts/ directory.

### 🛠️ Installation

Install the required packages:

pip install -r requirements.txt

### ▶️ How to Run

Open Jupyter Notebook:

jupyter notebook


Run the notebook flight_delay_eda.ipynb or your Python script.

Output charts are saved automatically to the artifacts/ folder.

### 📦 Project Structure

project_flight_delays_eda/
├─ notebooks/
│  └─ EDA_Flight_Delays.ipynb
├─ data/
│  └─ flights.csv          # user-provided BTS or Kaggle CSV
├─ artifacts/
│  ├─ dep_delay_distribution.png
│  ├─ median_delay_by_carrier.png
│  ├─ median_delay_by_origin.png
│  ├─ monthly_pct_on_time.png
│  ├─ delay_cause_totals.png
│  └─ flights_cleaned_snapshot.csv
├─ src/
│  └─ preprocessing.py
└─ README.md

### ⭐ Future Enhancements

Streamlit dashboard for interactive exploration

Predictive modeling for delay forecasting

Airport congestion scoring

Weather-impact simulation models
