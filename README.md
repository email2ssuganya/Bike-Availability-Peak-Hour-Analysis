# 🚲 Bike Sharing Availability Analysis (Power BI)

## 📌 Project Overview

This project analyzes **bike station availability** using a snapshot-based dataset to understand **bike shortages, capacity utilization, and peak-hour pressure**. The dashboard is built in **Power BI** and focuses on operational insights that help improve bike redistribution and service reliability.

---

## 🎯 Business Problem

Bike-sharing systems often face:

* Stations with **zero or low bike availability**
* Shortages during **peak demand hours**
* Inefficient redistribution of bikes across stations

This project aims to identify **where and why shortages occur** and provide **data-driven recommendations** to improve availability.

---

## 📂 Dataset Description

The dataset contains **station-level snapshot data**, including:

* Station ID and station name
* Total bike stands
* Available bikes
* Available bike stands
* Station status (Open/Closed)
* Date and time information
* Geographic coordinates (latitude & longitude)

> ⚠️ Note: The dataset represents a **single snapshot in time**, not a time series.

---

## 🧹 Data Cleaning & Transformation (Power Query)

* Standardized column names and data types
* Split DateTime into Date, Time, Hour, and Day Name
* Created **Peak Hour / Non-Peak Hour** indicator
* Handled missing and null values
* Split latitude and longitude from combined position field
* Validated bike availability against stand capacity

---

## 🧱 Data Modeling

* Used a **snapshot-based data model**
* Created a central table representing **current bike availability per station**
* Maintained station descriptive attributes
* Applied a **1:1 relationship** consistent with snapshot granularity
* Avoided unnecessary bidirectional filters

---

## 🧮 DAX Measures & Calculations

Key measures created include:

* Total Stations
* Total Available Bikes
* Total Bike Stands
* Average Utilization %
* Stations with Zero Bikes
* Low Availability Stations
* Peak Hour Available Bikes

### Calculated Column

* **Availability Category**: No Bikes / Low Availability / Available

---

## 📊 Dashboard Visuals

The Power BI dashboard includes:

* KPI cards with conditional color formatting
* Clustered bar charts for station comparison
* Donut chart showing availability distribution
* Scatter plot (Available Bikes vs Available Stands)
* Map visual for geographic distribution
* Peak vs Non-Peak availability comparison

---

## 📈 Key Insights (Data-Driven)

* ~**31% overall capacity utilization**, despite sufficient infrastructure
* **381 stations (~37%)** have **zero bikes available**
* **527 stations (~51%)** fall under **low availability**
* Bike availability drops sharply during **peak hours**
* Availability imbalance is caused by **redistribution inefficiency**, not lack of bikes

---

## 🔍 Types of Analysis Performed

* **Descriptive:** Current availability and utilization patterns
* **Diagnostic:** Reasons behind bike shortages and imbalance
* **Predictive:** Expected continuation of shortages during peak hours
* **Prescriptive:** Recommendations for proactive bike redistribution

---

## ✅ Recommendations

* Redistribute bikes **before peak hours** to zero-bike stations
* Prioritize stations with repeated low availability
* Move bikes from surplus to high-demand areas
* Use availability categories for operational monitoring
* Improve redistribution efficiency without adding infrastructure

---

## 🛠 Tools & Technologies

* Power BI Desktop
* Power Query (M)
* DAX
* Data Visualization & Dashboarding

---

## 🏁 Conclusion

This project demonstrates how snapshot-based data can be effectively used to identify operational issues in bike-sharing systems. By focusing on availability imbalance and peak-hour pressure, the dashboard supports actionable decision-making to improve service reliability.
