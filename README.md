# 🏎️ Formula 1 — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

An end-to-end exploratory data analysis of Formula 1 racing history — covering circuits, drivers, and constructors — using a rich dataset of 500,000+ records spanning from 2009 through 2017.

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Analysis Sections](#analysis-sections)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Key Visualisations](#key-visualisations)
- [Contributing](#contributing)

---

## Project Overview

This project dives deep into the world of Formula 1 using publicly available race data. The goal is to uncover patterns, trends, and stories hidden within decades of racing statistics — from which circuits host the most races and what climate zones they sit in, to which drivers rack up the most wins and which constructors dominate the championship.

---

## Dataset

The dataset consists of **14 CSV files** (~521,000 rows combined):

| File | Description | Rows |
|---|---|---|
| `circuits.csv` | Track metadata — location, country, coordinates | 72 |
| `races.csv` | Race calendar per season | 997 |
| `drivers.csv` | Driver profiles and nationalities | 841 |
| `results.csv` | Race-by-race finishing results | 23,776 |
| `driverStandings.csv` | Championship standings per driver per race | 31,726 |
| `constructors.csv` | Constructor (team) metadata | 208 |
| `constructorStandings.csv` | Championship standings per constructor | 11,896 |
| `constructorResults.csv` | Points scored per constructor per race | 11,142 |
| `lapTimes.csv` | Lap-by-lap timing data | 426,633 |
| `pitStops.csv` | Pit stop events and durations | 6,251 |
| `qualifying.csv` | Q1/Q2/Q3 qualifying session times | 7,516 |
| `seasons.csv` | Season metadata | 69 |
| `status.csv` | Race finish status codes | 134 |

> **Source:** Ergast Developer API (F1 historical data up to 2017)

---

## Project Structure

```
f1-eda/
│
├── F1-EDA.ipynb              # Main analysis notebook
│
├── race-data/                # Primary dataset
│   ├── circuits.csv
│   ├── constructorResults.csv
│   ├── constructorStandings.csv
│   ├── constructors.csv
│   ├── driverStandings.csv
│   ├── drivers.csv
│   ├── lapTimes.csv
│   ├── pitStops.csv
│   ├── qualifying.csv
│   ├── races.csv
│   ├── results.csv
│   ├── seasons.csv
│   └── status.csv
│
├── insights.md               # Key findings and takeaways
├── requirements.txt          # Python dependencies
├── .gitignore
└── README.md
```

---

## Analysis Sections

### 🌍 1. Circuits
- Interactive world map of all F1 circuits using clustered markers (Folium)
- Top 10 countries by number of hosted circuits
- Most frequently held Grand Prix races
- Climate zone distribution of all circuits

### 🧑‍🏎️ 2. Drivers
- Average points scored by drivers (post-2010) — bubble chart by total points
- All-time most Formula 1 victories per driver
- Pairwise relationships between driver stats (wins vs. lap times)
- Driver finish status and fastest lap correlations
- Best pit stop performers by duration
- Geographic breakdown of veteran vs. younger generation drivers

### 🏗️ 3. Constructors
- Nationality breakdown of all F1 constructors
- Constructors with the most race wins (radar chart + bar chart + pie chart)
- Total points accumulated by each constructor over all seasons

---

## Tech Stack

| Library | Purpose |
|---|---|
| `pandas` | Data loading, merging, and aggregation |
| `numpy` | Numerical operations |
| `plotly` | Interactive bar charts, pie charts, radar charts |
| `folium` | Interactive geographic map with circuit clusters |
| `seaborn` | Statistical visualisations |
| `matplotlib` | Bubble charts and general plotting |

---

## Getting Started

### Prerequisites
- Python 3.8 or higher
- pip

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/f1-eda.git
cd f1-eda

# 2. (Optional) Create a virtual environment
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the notebook
jupyter notebook F1-EDA.ipynb
```

---

## Key Visualisations

- **World Circuit Map** — Folium cluster map pinpointing every F1 circuit globally
- **Bubble Chart** — Average points vs. races driven, bubble size = total career points (post-2010 drivers)
- **Radar Chart** — Head-to-head comparison of top 5 constructors by race wins
- **Climate Donut** — Breakdown of circuit climate zones (Marine West Coast dominates)
- **Pit Stop Bar Chart** — Fastest pit stop durations ranked by driver

---

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

*Data covers the 2009–2017 Formula 1 seasons via the Ergast Developer API.*
