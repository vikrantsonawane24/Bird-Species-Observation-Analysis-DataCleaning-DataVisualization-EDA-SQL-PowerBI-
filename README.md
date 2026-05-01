# 🐦 Bird Species Observation Analysis

> End-to-end data analytics project covering data cleaning, EDA, SQL database loading, and interactive Power BI dashboards for bird species observation data.

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Project Structure](#️-project-structure)
- [Tech Stack](#️-tech-stack)
- [Dashboard Pages](#-dashboard-pages)
- [Data Pipeline](#️-data-pipeline)
- [How to Run](#-how-to-run)
- [Key Insights](#-key-insights)
- [Author](#-author)
- [License](#-license)

---

## 📌 Project Overview

This project analyzes bird species observation records collected across multiple national parks and habitats. It covers the complete data pipeline — from raw CSV ingestion and Python-based cleaning, through SQL storage, to multi-page Power BI visualizations.

**Key Stats from the Dashboard:**
- 🔢 **17K** Total Observations
- 🐦 **126** Unique Species
- 🌲 **9K** Forest Observations
- 🌿 **9K** Grassland Observations

---

## 🗂️ Project Structure

```
Bird-Species-Observation-Analysis/
│
├── data/
│   ├── raw/                  # Original CSV files
│   └── cleaned/              # Cleaned and merged datasets
│
├── notebooks/
│   └── EDA_cleaning.ipynb    # Data cleaning & exploratory analysis
│
├── sql/
│   └── load_data.py          # PostgreSQL data loading via psycopg2/SQLAlchemy
│
├── powerbi/
│   └── Bird_Species_Dashboard.pbix   # Power BI dashboard file
│
└── README.md
```

---

## 🛠️ Tech Stack

| Layer | Tools Used |
|---|---|
| Data Cleaning & EDA | Python, Pandas, Jupyter Notebook |
| Database | PostgreSQL (pgAdmin) |
| DB Connectivity | psycopg2, SQLAlchemy |
| Visualization | Power BI Desktop |

---

## 📊 Dashboard Pages

### Page 1 — Overview
- Total Observations KPI cards (17K total, 126 species, 9K Forest, 9K Grassland)
- Observations by Park (top park: ANTI with ~4K observations)
- Observations by Season (Summer: 67.23%, Spring: 32.77%)
- Total Observations by Year (2018)
- Total Observations by Habitat (Forest vs Grassland)

### Page 2 — Species Analysis
- Top 15 species by observation count broken down by habitat (Forest/Grassland)
- Top species: Northern Cardinal, Carolina Wren, Red-eyed Vireo
- Sex Ratio: Male (79.6%), Undetermined (19.55%), Female (0.85%)
- Species count by Habitat (Forest ~100, Grassland ~100 unique species)
- ID Method breakdown: Singing > Calling > Visualization

### Page 3 — Temporal & Behavioral Trends
- Monthly Observation Trends (May → June peak → July dip)
- Observations by Season & Habitat (Summer dominates both Forest and Grassland)
- Peak Observation Hours (7 AM and 8 AM are busiest)
- Interval Length Distribution (0–2.5 min intervals are most common)

### Page 4 — Observer & Field Conditions
- Top Observers: Elizabeth Oswald, Kimberly Serno, Brian Swimelar
- Flyover vs Non-Flyover: 91.3% Non-Flyover observations
- Observation Distance Distribution (50–100 meters is most common range)
- Watchlist Species by Habitat (Forest has more watchlist species than Grassland)

### Page 5 — Environmental Conditions
- Sky Condition Impact: Partly Cloudy and Clear skies yield most observations
- Regional Stewardship Status: 76.66% True stewardship areas
- Wind Condition Impact: Light air movement (1–3 mph) = highest observations
- Disturbance Effect: Majority of sessions had "No effect on count"

---

## ⚙️ Data Pipeline

```
Raw CSV Files
     ↓
Python (Pandas) — Cleaning, Merging, EDA
     ↓
PostgreSQL — Structured storage via psycopg2 / SQLAlchemy
     ↓
Power BI — Connected via PostgreSQL connector
     ↓
Interactive 5-Page Dashboard
```

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/vikrantsonawane24/Bird-Species-Observation-Analysis-Data-Cleaning-Data-Visualization-EDA-SQL-PowerBI-.git
cd Bird-Species-Observation-Analysis-Data-Cleaning-Data-Visualization-EDA-SQL-PowerBI-
```

### 2. Run the Jupyter Notebook
```bash
jupyter notebook notebooks/EDA_cleaning.ipynb
```

### 3. Load Data into PostgreSQL
```bash
python sql/load_data.py
```

### 4. Open Power BI Dashboard
- Open `powerbi/Bird_Species_Dashboard.pbix` in Power BI Desktop
- Update the PostgreSQL connection string to your local setup if needed

---

## 📈 Key Insights

- **ANTI** (Antietam) park has the highest number of bird observations (~4K)
- **Summer** is the dominant observation season at 67.23%
- **Northern Cardinal** and **Carolina Wren** are the most frequently observed species
- Most birds are identified by **singing** rather than visual sighting
- Optimal conditions for observation: **partly cloudy skies**, **light wind**, **7–8 AM hours**
- **91.3%** of observations are non-flyover, indicating stationary or nearby activity

---

## 👤 Author

**Vikrant Sonawane**
- 📍 Kalyan, Maharashtra, India
- 📧 vikrantsonawane24@gmail.com
- 🔗 https://www.linkedin.com/in/vikrantsonawane24/

---

## 📄 License

This project is for educational and portfolio purposes.
