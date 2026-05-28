
# 🏥 FP20 Analytics August 2025 Challenge

## Athlete Health & Injury Analytics Dashboard (Power BI)

**Status:** Completed — Full data model, relationships, DAX measures, and interactive dashboard pages developed.

---

# 📌 About This Project

This project is my submission for the **FP20 Analytics August 2025 Challenge** in collaboration with **ZoomCharts**, focused on analyzing an **Athlete Health & Injury Dataset** using Power BI.

The challenge simulates real-world sports analytics requirements where leagues, clubs, coaches, medical teams, and executives rely on injury intelligence to improve athlete availability, reduce recovery downtime, optimize treatment effectiveness, and manage financial impact.

The project emphasizes:

* Complex dimensional data modeling
* Relationship optimization
* Conformed dimensions handling
* DAX performance optimization
* Business storytelling through sports analytics
* Interactive Power BI dashboard design

### 🔗 Challenge Link

https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/challenges/fp20-analytics-august-2025

---

# 🖼️ Dashboard Preview

## Data Model

<img width="895" height="728" alt="Image" src="https://github.com/user-attachments/assets/db16808c-45e2-467a-bb4e-1e577f48dba7" />

## Dashboard Pages 1- 2 -3

<img width="1920" height="3240" alt="Image" src="https://github.com/user-attachments/assets/8b2a2fff-d5b7-4727-ba7c-089365242d67" />

---

# 🗂️ Data Model

The solution follows a **Star Schema Architecture** centered around the `FactInjuries` table connected with multiple dimension tables for athlete, event, treatment, location, coach, and injury analysis.

## Tables Loaded

| Table Name      | Description                        |
| --------------- | ---------------------------------- |
| `FactInjuries`  | Injury-level transactional records |
| `DimPlayer`     | Athlete demographic information    |
| `DimInjuryType` | Injury classification and severity |
| `DimClub`       | Club and competition details       |
| `DimCoach`      | Coach and trainer information      |
| `DimLocation`   | Geographic analysis dimensions     |
| `DimTreatment`  | Treatment methods and outcomes     |
| `DimEvent`      | Event and competition tracking     |

---

## Fact Table

### `FactInjuries`

Contains injury-level transactional records including:

* Injury ID
* Injury Date
* Estimated Days Absent
* Days to Recovery
* Treatment Cost
* Event references
* Coach references
* Club references
* Injury type references

---

## Dimension Tables

### `DimPlayer`

Player demographics and athlete segmentation

* Age
* Age Group
* Gender
* PlayerDimKey

### `DimInjuryType`

Detailed injury classification

* Injury Type
* Injury Cause
* Severity
* Body Part
* Recurring Injury Flag

### `DimClub`

Club and competition information

* Club/Team Name
* Competition Level
* Sport
* Surface Type

### `DimCoach`

Coaching and trainer details

* Coach/Trainer Name

### `DimLocation`

Geographical analysis dimensions

* Country
* Region
* Latitude
* Longitude

### `DimTreatment`

Treatment effectiveness analysis

* Treatment Method
* Outcome

### `DimEvent`

Event-based injury tracking

* Event Name
* Event Type

---

# 🔗 Relationships

The model uses **One-to-Many relationships** from dimension tables into the central fact table to maintain optimized filtering and analytical performance.

## Relationships Overview

| From                          | To                             | Status   |
| ----------------------------- | ------------------------------ | -------- |
| `FactInjuries[PlayerDimKey]`  | `DimPlayer[PlayerDimKey]`      | ✅ Active |
| `FactInjuries[InjuryTypeKey]` | `DimInjuryType[InjuryTypeKey]` | ✅ Active |
| `FactInjuries[ClubKey]`       | `DimClub[ClubKey]`             | ✅ Active |
| `FactInjuries[CoachKey]`      | `DimCoach[CoachKey]`           | ✅ Active |
| `FactInjuries[LocationKey]`   | `DimLocation[LocationKey]`     | ✅ Active |
| `FactInjuries[TreatmentKey]`  | `DimTreatment[TreatmentKey]`   | ✅ Active |
| `FactInjuries[EventKey]`      | `DimEvent[EventKey]`           | ✅ Active |

### Key Relationship Design Features

* Centralized fact table architecture
* Conformed dimensions for reusable filtering
* Optimized cardinality management
* Single-direction filtering for performance
* Scalable schema design for future expansion

---

# 📐 DAX Measures & KPIs

The dashboard includes multiple analytical measures focused on athlete welfare, operational efficiency, and financial impact.

## Injury Analytics

* Total Injuries
* Injury Frequency
* Recurring Injury %
* Severe Injury Count
* Injury Rate by Sport
* Injury Distribution by Event

## Recovery & Treatment Analytics

* Average Recovery Days
* Recovery Time by Injury Type
* Treatment Success Rate
* Average Treatment Cost
* Cost per Recovery Day

## Athlete Availability Metrics

* Estimated Days Absent
* Player Availability %
* Recovery Efficiency
* Injury Downtime Trends

## Demographic Insights

* Injury Rate by Gender
* Injury Rate by Age Group
* Injury Severity by Athlete Segment

## Geographic & Team Insights

* Regional Injury Distribution
* Injury Trends by Country
* Team-wise Injury Analysis
* Coach-wise Injury Performance

---

# 📊 Dashboard Features

## Page 1 — Injury & Health Overview

### Visuals Included

* KPI Cards:

  * Total Injuries
  * Average Recovery Days
  * Total Treatment Cost
  * Severe Injury %

* Trend analysis of injuries over time

* Injury distribution by sport

* Injury severity analysis

* Recovery duration comparison

* Geographic injury heatmap

* Team and competition-level analysis

---

## Page 2 — Recovery & Performance Insights

### Visuals Included

* Treatment effectiveness analysis
* Recovery performance by injury type
* Coach-wise injury comparison
* Athlete demographic analysis
* Surface type vs injury frequency
* Event-based injury occurrence
* Interactive drill-down filtering experience

---

# 🎯 Business Questions Explored

This dashboard helps answer critical sports analytics questions such as:

* Which injuries occur most frequently?
* Which sports generate the highest injury rates?
* How does injury severity vary by athlete demographics?
* Which treatment methods improve recovery speed?
* Are injuries influenced by playing surfaces or competition level?
* Which regions or teams experience higher injury frequency?
* Which coaches maintain lower injury rates?

---

# ⚙️ Tools & Technologies Used

* Power BI Desktop
* Power Query
* DAX (Data Analysis Expressions)
* Data Modeling
* ZoomCharts Custom Visuals
* Star Schema Design

---

# 🚀 Key Skills Demonstrated

* Advanced Power BI dashboard development
* Sports analytics storytelling
* Dimensional data modeling
* Complex relationship handling
* DAX optimization
* KPI engineering
* Interactive report design
* Business intelligence reporting

---

# 📈 Project Outcomes

This project demonstrates how analytics can support:

* Improved athlete health management
* Reduced recovery downtime
* Better financial control over treatment costs
* Enhanced player availability
* Data-driven coaching and medical decisions
* Competitive performance optimization

---

# 🤝 Acknowledgements

Dataset and challenge provided by **FP20 Analytics** in partnership with **ZoomCharts**.

Challenge focused on building advanced analytical solutions for athlete injury intelligence and sports performance optimization using Power BI.

---

Built with **Power BI Desktop**.
