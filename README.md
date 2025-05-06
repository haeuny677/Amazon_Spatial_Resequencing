# 📦 Amazon Last-Mile Delivery: Spatial Delay Optimization

This project analyzes urban last-mile delivery delays using Amazon’s 2021 Last Mile Routing Research Challenge dataset. We applied spatial and statistical techniques to identify inefficiencies and propose route re-sequencing solutions for high-risk areas.

## 🚀 Objective
To identify spatial patterns of delivery delays in major U.S. cities and optimize routing strategies to improve efficiency and reduce congestion.

## 🔍 Business Questions
- What factors most influence delivery efficiency?
- Where are the highest congestion zones?
- Can weighted route re-sequencing reduce delays in urban areas?

## 🧰 Tools & Technologies
- **Language:** R, Python
- **Methods:** PCA, K-Means Clustering, Regression, HDBSCAN, Weighted TSP
- **Libraries:** `tidyverse`, `ggplot2`, `cluster`, `dbscan`, `geopandas`
- **Mapping:** QGIS, Folium
- **Data Source:** [Amazon Last Mile Routing Research Challenge (2021)](https://www.amazon.science/competitions/amazon-last-mile-routing-research-challenge)

## 🗂 Data Overview
- 9,184 historical routes with stop- and package-level features
- Cities: Los Angeles, Seattle, Boston, Austin, Chicago
- Merged & cleaned 3 JSON files
- Engineered new variables (delivery duration, load utilization, packages per stop)

## 🧪 Methodology
### 📉 PCA & Clustering
- Applied PCA to reduce dimensionality (captured 70% variance)
- Used K-means to identify 3 operational patterns
- Key contributing factors: Load Utilization, Planned Service Time, Delivery Duration

### 📈 Regression
- Load Utilization had a small negative impact on delivery time
- More packages per stop slightly increased time

### 🗺 Spatial Analysis
- Mapped delivery delay hotspots using HDBSCAN
- Identified congestion zones in downtown/commercial areas (e.g., LA, Seattle, Boston)
- Generated risk scores by cluster

## 🚚 Optimization Strategy
- Proposed **Weighted TSP** route re-sequencing in high-risk clusters
- Incorporated **time-of-day penalties** for smarter delivery scheduling

## ⚠️ Limitations
- Re-sequencing is static; does not account for live traffic or weather
- TSP uses fixed weights; lacks predictive adaptability

## 🌟 Future Enhancements
- Integrate predictive models to forecast delay risk and load
- Real-time rerouting engine using traffic + forecast data
- Multi-objective optimization: balance delay, utilization, and service time

---

> 📍 Developed by HaEun Yoon, Minji Song, Sangyeon Lee, Yuchen Ni, Zixin Liu
