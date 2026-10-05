# US & International Air Traffic Analysis (BigQuery SQL + Tableau)

Airline network and capacity analysis built on two U.S. DOT datasets, modelled in Google BigQuery and reported in a Tableau dashboard. Framed as a planning brief for an airline strategy team: where demand sits, when it peaks, and how it reacts to shocks.

**Stack:** Google BigQuery (SQL), Python (pandas, matplotlib, seaborn), Tableau  
**Context:** Team project, BA775 Business Analytics Toolbox, Boston University Questrom.

## Business questions
1. How have international passenger volumes trended since 1990, and how hard did major shocks hit?
2. Which routes, hubs and carriers carry the most traffic?
3. How strong is seasonality at the busiest airports, and when should capacity be added?
4. How did freight behave when passenger demand collapsed?

## Data
- [U.S. Airline Traffic by Airport](https://www.bts.gov/browse-statistical-products-and-data/state-transportation-statistics/us-airline-traffic-airport) (BTS): passengers and freight by airport for five states (CA, AK, IL, MA, GA)
- [International Report: Passengers](https://data.transportation.gov/Aviation/International_Report_Passengers/xgub-n9bw/about_data) (U.S. DOT): passengers by U.S. gateway, foreign airport and carrier

## Approach
- Combined the five state tables into one BigQuery table with `UNION ALL`, then profiled and fixed nulls with SQL
- Designed an ERD linking U.S. airports (`Code`) to international routes (`usg_apt`), and used `LEFT JOIN`s to find airports present in one source but not the other
- Wrote aggregate SQL for YoY change, carrier market share, top routes and monthly seasonality
- Built an executive Tableau dashboard on top of the query outputs

## Key findings
- International passengers grew steadily from 1990 to 2019, with dips after 9/11 (about -9%) and the 2008 crisis (about -5.9%), then fell **73.8% in 2020**
- Demand peaks in **Q2 and Q3**; JFK to LHR is the single heaviest route, followed by JFK to CDG and LAX to LHR
- **American (13.3%), United (9.7%) and Delta (8.7%)** hold the largest passenger shares among named carriers
- LAX, ORD, SFO and BOS are the main international gateways; California leads on passengers and freight, Alaska stands out as a freight hub
- Freight held up and grew while passenger traffic collapsed during COVID

## Recommendations
- Add frequency and larger gauge on JFK/LAX to LHR in Q2 and Q3
- Use freight capacity as a hedge when passenger demand is shocked
- Track route-level demand monthly to reallocate capacity ahead of seasonal peaks

## Dashboard
[Tableau Public: International Aviation Industry Report](https://public.tableau.com/app/profile/junhan.chen7027/viz/BA775B04InternationalAirportAnalysis20243nd/Dashboard1)

## Repo contents
- `US-Air-Traffic-Analysis.ipynb`: SQL queries, outputs and charts (runs in Colab against BigQuery)
- `requirements.txt`
