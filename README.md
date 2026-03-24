# Ship Fuel Consumption Anomaly Detection

**Author:** Amna Riaz | Dalian Maritime University | MSc Artificial Intelligence

## Overview
This project detects ships consuming abnormally high fuel relative to their route, 
distance, weather, and engine efficiency using unsupervised machine learning. 
Identifying fuel anomalies helps ship operators reduce costs and cut unnecessary 
CO2 emissions before they escalate.

## Dataset
Ship fuel efficiency data from Nigerian waterways — 1,440 operational records 
across 4 ship types: Tanker Ship, Fishing Trawler, Oil Service Boat, and Surfer Boat.

## Problem
There are no predefined labels for abnormal fuel consumption making this an 
unsupervised learning problem. Traditional fixed threshold systems flag any vessel 
consuming more than X liters regardless of route, distance, or weather context — 
producing too many false alarms.

## Solution
Isolation Forest anomaly detection that learns the normal consumption pattern for 
each ship type, route, and weather condition, then flags deviations from that 
learned pattern. This is smarter than fixed thresholds because it considers full 
operational context before flagging.

## Results
| Metric | Value |
|---|---|
| Total records analyzed | 1,440 |
| Normal operations | 1,368 (95%) |
| Anomalies detected | 72 (5%) |
| Ship type affected | Tanker Ships only |

## Key Finding
All 72 detected anomalies belonged exclusively to Tanker Ships, suggesting 
systematic over-consumption specific to this vessel type on Nigerian waterways. 
Anomalous tankers showed significantly higher fuel consumption and CO2 emissions 
compared to normal operations on similar routes and distances.

## Technologies
Python, Scikit-learn, Isolation Forest, Pandas, Matplotlib, Seaborn, StandardScaler

## Real World Impact
Ship operators can inspect inefficient vessels before fuel costs escalate. 
Environmental agencies can target CO2 reduction efforts at highest impact vessels. 
This approach is scalable to any waterway globally with minimal modification.
