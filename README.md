# US Air Traffic Analysis

## Overview
This project presents a detailed analysis of international passenger and U.S. air traffic to provide actionable insights for airlines' strategic decision‑making. Using datasets from the U.S. Department of Transportation’s “U.S. Airline Traffic by Airport” and “International Passenger Report,” it explores passenger volumes, freight loads, seasonality and market share trends over the past decade.

## Data
- **U.S. Airline Traffic by Airport:** Annual and monthly passenger counts and freight loads for U.S. airports.
- **International Passenger Report:** Passenger counts by origin and destination for international routes.

## Objectives
- Compare and integrate data from the two datasets to identify unique and overlapping airports.
- Calculate annual passenger volumes and assess year‑over‑year changes.
- Analyze passenger and cargo destinations to highlight popular routes.
- Investigate seasonal variations in passenger volumes at the top five busiest U.S. airports.
- Examine freight load trends and the impact of major events (e.g., COVID‑19 pandemic).

## Methodology
1. **Data preparation:** Clean and merge datasets for California, Alaska, Illinois, Massachusetts, and Georgia; handle null values and standardize formats.
2. **Exploratory analysis:** Use SQL and Python (pandas/matplotlib) to compute metrics and visualize trends.
3. **Visualizations:** Generate line charts for passenger volume over time, bar charts for market share by carrier, and seasonality plots for top airports.

## Key Findings
- Passenger volumes increased steadily over the decade but dropped sharply in 2020 (≈ 74 % decline) due to the COVID‑19 pandemic.
- Seasonal peaks occur in Q2–Q3, especially on transatlantic routes such as JFK–LHR and JFK–CDG.
- American Airlines and United Airlines hold the largest international market shares; freight loads surged during 2020–2021.

## Usage
1. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. Open the notebook:

   ```bash
   jupyter notebook us_air_traffic_analysis.ipynb
   ```

3. Execute the cells to reproduce the analysis and plots.

## Recommendations
- Adopt dynamic scheduling and resource allocation to adjust to seasonal demand and global events.
- Optimize high‑demand routes by increasing flight frequencies and capacity during peak seasons.
- Diversify revenue streams by expanding freight operations and partnering with logistics companies.
- Continuously analyze passenger and freight data to anticipate market trends and enhance strategic planning.
