# Air Quality EDA & Visualization

> Exploratory Data Analysis and Visualization of Global Air Pollution Patterns

**Anoushka Karra** • Chaitanya Bharathi Institute of Technology (A) • EDAV [22ADC31N]

---

## Overview

This project analyzes daily air pollution records from major cities worldwide, transforming raw environmental data into actionable insights through systematic EDA, statistical testing, machine learning, and risk modeling.

---

## Project Workflow

| Step | Phase | Description |
|------|-------|-------------|
| 1 | Data Collection | Kaggle dataset — `city_day.csv` |
| 2 | Data Cleaning | Duplicates, nulls, IQR outlier removal |
| 3 | Feature Engineering | Temporal features, Season (hemisphere-aware), IsWeekend |
| 4 | Exploratory Data Analysis | 1D, pairwise, and integrated visualizations |
| 5 | Statistical Testing | Mann–Whitney U test (weekday vs weekend) |
| 6 | Machine Learning | K-Means clustering on city pollution profiles |
| 7 | Risk Modeling | PCA-based composite risk score + classification |
| 8 | Predictive Modeling | Random Forest PM2.5 forecasting |

---

## Dataset

| Field | Details |
|-------|---------|
| **Source** | [Kaggle — Air Quality in Biggest Cities of the World](https://www.kaggle.com/) by efimpolianskii |
| **File** | `city_day.csv` |
| **Size** | 43,450 rows × 13 columns |
| **Pollutants** | PM2.5, PM10, NO₂, SO₂, CO, O₃ |
| **Coverage** | Multiple countries, multiple years |

**Columns:** `Country Code`, `City`, `Location`, `Coordinates`, `Pollutant`, `Value (µg/m³)`, `Last Updated`, `Country Label`, `Lat`, `Long`

---

## Key Analyses

### Exploratory Analysis
- Distribution of pollutant concentration values
- Pollutant type breakdown (pie chart)
- Top 10 most polluted cities by average concentration
- Records per year (temporal coverage)
- Pollutant concentration by type (violin plots)
- Average pollution by season
- Integrated heatmaps — pollutant type vs season
- Pollutant correlation matrix

### Analytical Questions
| # | Question |
|---|----------|
| Q1 | Does pollutant concentration vary by country and pollutant type? |
| Q2 | How has pollution intensity evolved over time? |
| Q3 | How do pollution levels differ between weekdays and weekends? |
| Q4 | How does PM2.5 distribution vary across months? (Ridgeline plot) |
| Q5 | How do seasonal PM2.5 patterns vary across major cities? (3D surface) |
| Q6 | How dominant are fine particles (PM2.5) vs coarse particles (PM10)? |
| Q7 | Are extreme pollution events linked to specific pollutant types and seasons? |

### Machine Learning & Risk Modeling
- **K-Means Clustering** — cities grouped into 4 pollution profiles (elbow method used to select K)
- **PCA Risk Score** — composite 0–1 risk index derived from multi-pollutant variance
- **Risk Classification** — Low / Moderate / High / Severe categories
- **Random Forest** — PM2.5 prediction using month, season, city, and day-of-week features

---

## Key Findings

- **Winter dominance** — PM2.5 and PM10 peak in winter due to temperature inversions and heating activity
- **Geographic disparity** — India and Turkey show 3–4× higher concentrations than Chile and Australia
- **Weekday effect** — NO₂ and CO are statistically higher on weekdays (Mann–Whitney U, p < 0.05)
- **Fine particle risk** — Many cities show PM2.5/PM10 ratios above 0.5, indicating serious health concern
- **4 city clusters** — cities group into distinct pollution profiles requiring different mitigation strategies
- **WHO exceedances** — most cities exceed WHO PM2.5 guideline of 5 µg/m³ significantly

---

## Real World Impact

| Domain | Application |
|--------|-------------|
| Environmental Policy | Prioritize high-risk cities for targeted regulation |
| Urban Traffic Management | Design low-emission zones using weekday/weekend patterns |
| Public Health Monitoring | Issue seasonal alerts during winter peak periods |
| Urban Planning | Use pollution risk maps for zoning and green corridor placement |
| Pollution Forecasting | Temporal patterns serve as baseline for predictive models |

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikit-learn)

| Library | Purpose |
|---------|---------|
| `pandas` | Data manipulation and aggregation |
| `numpy` | Numerical operations |
| `matplotlib` | Base plotting and 3D visualization |
| `seaborn` | Statistical visualizations |
| `scikit-learn` | K-Means clustering, PCA, Random Forest |
| `scipy` | Mann–Whitney U statistical test |

---

## Project Structure

```
air-quality-eda/
│
├── data/
│   └── city_day.csv                        # Raw dataset (download from Kaggle)
│
├── Air_Quality_EDA_Visualization.ipynb     # Main Jupyter notebook
├── Air_Quality_EDA_Visualization.py        # Script export of the notebook
└── README.md
```

---

## How to Run

**1. Clone the repository**
```bash
git clone https://github.com/your-username/air-quality-eda.git
cd air-quality-eda
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
```

**3. Download the dataset**

Download `city_day.csv` from [Kaggle](https://www.kaggle.com/) and place it inside the `data/` folder.

**4. Run the notebook**
```bash
jupyter notebook Air_Quality_EDA_Visualization.ipynb
```

Or run as a script:
```bash
python Air_Quality_EDA_Visualization.py
```

---

## Limitations

- Missing data for some city–pollutant–time combinations
- Season assignment based on hemisphere (Northern/Southern) — no sub-equatorial fine-tuning
- No meteorological variables (wind, humidity, temperature) to support causal inference
- Inconsistent temporal coverage across cities and years

---

## Future Work

- Integrate meteorological data for deeper causal analysis
- Extend predictive modeling to other pollutants with sufficient data
- Build an interactive Streamlit dashboard for public exploration
- Correlate pollution trends with epidemiological health outcome data
- Apply source-apportionment techniques to trace emission origins

---

## Acknowledgements

Dataset sourced from Kaggle — *Air Quality in Biggest Cities of the World* by efimpolianskii.  
Project submitted as part of the EDAV [22ADC31N] Course End Project,  
Department of Information Technology, CBIT (A), AY 2025–26.
