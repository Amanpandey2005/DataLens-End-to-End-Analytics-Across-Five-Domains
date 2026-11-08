# DataLens: End-to-End Analytics Across Five Domains

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![R](https://img.shields.io/badge/R-4.0%2B-276DC3)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A portfolio of five end-to-end data analytics and data science projects spanning pandemic epidemiology, real estate economics, global security, sports statistics, and quantitative finance. Every project follows the same rigorous workflow: **problem formulation → data acquisition → cleaning → exploratory analysis → modeling → interpretation.**

---

## Table of Contents

- [About](#about)
- [Projects Overview](#projects-overview)
- [Results Snapshot](#results-snapshot)
- [Project Details](#project-details)
- [Technology Stack](#technology-stack)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## About

DataLens is a curated collection of analytics projects built across very different domains, using both Python and R. Together they demonstrate:

- Statistical modeling (OLS, linear mixed models, diagnostic testing)
- Machine learning (ensemble regression, imputation, feature engineering)
- Geospatial analysis and rich visualization
- Financial time-series analytics and Monte Carlo simulation

## Projects Overview

| # | Project | Domain | Language | Focus |
|---|---------|--------|----------|-------|
| 1 | COVID-19 Pandemic Analysis | Public Health | Python | Pandemic visualization and EDA |
| 2 | Flats in Cracow | Real Estate | Python | Price prediction with ensemble ML |
| 3 | Global Terrorism Database | Security / Policy | R | Geospatial EDA and trend analysis |
| 4 | Polar Watch: Workout Vitals | Sports Analytics | Python | Statistical modeling of fitness data |
| 5 | Trading Results Analysis | Quantitative Finance | Python | Algorithm performance and risk metrics |

## Results Snapshot

| Project | Key Result |
|---------|------------|
| COVID-19 | ~35M cases analyzed; rural population vs. cases correlation: -0.46 |
| Cracow Real Estate | VotingRegressor ensemble outperformed MLP, GBR, and baseline |
| Global Terrorism | 11-year EDA; ISIL, Taliban, Al-Qaida among deadliest groups |
| Polar Watch | Mixed model RMSE 61 vs. 79 (OLS); 283 workouts analyzed |
| FX Trading | 92 trades; 40% win rate; Monte Carlo with 100K simulations |

---

## Project Details

### 1. COVID-19 Pandemic Analysis

A multi-notebook exploratory analysis of the COVID-19 pandemic. It combines JHU CSSE case time series with World Bank socioeconomic indicators to uncover trends across time, geography, and population health metrics.

**Key highlights**
- Global scale: ~35M confirmed cases analyzed as of October 2020
- Multi-level analysis: world, continent, and country breakdowns
- Socioeconomic integration: GDP, life expectancy, rural population, healthcare expenditure
- Reusable architecture: custom `CovidDataViz` class for reproducible plotting

**Folder:** `covid19-pandemic-analysis/`

### 2. Flats in Cracow

A complete data science workflow for predicting residential flat sale prices in Cracow, Poland, from web-scraped listings through cleaning, EDA, feature engineering, and ensemble regression.

**Key highlights**
- Ensemble modeling: `VotingRegressor` combining MLP and Gradient Boosting
- Feature engineering: 8+ derived features including log-transforms and ratios
- Preprocessing: KNN imputation, one-hot encoding, min-max scaling
- Interpretability: district-level analysis showing central vs. outlying area premiums

**Folder:** `cracow-real-estate-pricing/`

### 3. Global Terrorism Database

Exploratory and geospatial analysis of the Global Terrorism Database (2007-2017), covering attack patterns, casualties, weapon and target types, and the most active organizations.

**Key highlights**
- 11-year window filtered to confirmed terrorist incidents
- Annotation-style maps of group activity
- Analysis across time, geography, attack type, weapon, target, and perpetrator
- Faceted time series, correlation matrices, tile plots, and stacked area charts

**Folder:** `global-terrorism-eda/`

### 4. Polar Watch: Workout Vitals

Statistical analysis of workout data exported from a Polar watch, examining heart-rate distributions, caloric expenditure, session duration, and differences between strength and cardio activity.

**Key highlights**
- 283 workouts analyzed over ~1 year
- OLS regression, linear mixed models, VIF, Goldfeld-Quandt, Shapiro-Wilk, Q-Q plots
- Strength vs. cardio heart-rate profiles
- Caloric modeling: RMSE 79 (OLS) → 61 (mixed model), R² up to 0.98 by sport

**Folder:** `polar-watch-fitness-analysis/`

### 5. Trading Results Analysis

Walk-forward performance analysis of an algorithmic trading system, evaluating profitability, risk, trade duration, and statistical properties of returns.

**Key highlights**
- 92 trades analyzed across multiple FX instruments
- Monte Carlo simulation with 100,000 samples for forward performance estimates
- Profit-per-lot distribution analysis (skew, kurtosis, fitted distributions)
- Profitable intraday timing patterns identified (2pm, 4pm)

**Folder:** `fx-trading-analysis/`

---

## Technology Stack

### Languages and Core Tools

| Tool | Purpose |
|------|---------|
| Python 3.8+ | Primary language for 4 of 5 projects |
| R 4.0+ | Global Terrorism analysis |
| Jupyter Notebooks | All analysis and modeling |
| Git | Version control |

### Python Libraries

| Library | Purpose | Projects |
|---------|---------|----------|
| Pandas | Data manipulation | All Python projects |
| NumPy | Numerical computing | All Python projects |
| Matplotlib | Visualization | All projects |
| Scikit-learn | ML preprocessing and modeling | Flats in Cracow |
| Statsmodels | Statistical modeling | Polar |
| SciPy | Statistics and distributions | Polar, Trading |
| wbdata | World Bank API access | COVID-19 |
| tabulate | Table formatting | Polar |

### R Libraries

| Library | Purpose |
|---------|---------|
| tidyverse (dplyr, ggplot2, tidyr) | Data manipulation and visualization |
| GGally | Matrix and pair plots |
| rworldmap / mapproj | Geospatial visualization |
| ggrepel | Non-overlapping text labels |
| lubridate | Date handling |
| scales | Axis formatting |

---

## Getting Started

### Prerequisites

- Python 3.8+
- R 4.0+ (only for the Global Terrorism project)
- Jupyter Notebook or JupyterLab

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/datalens.git
cd datalens

# Install Python dependencies (example: Flats in Cracow)
pip install pandas numpy matplotlib scikit-learn joblib
```

```r
# Install R dependencies (Global Terrorism)
install.packages(c("tidyverse", "GGally", "rworldmap", "ggrepel", "mapproj", "lubridate", "scales"))
```

### Requirements by Project

| Project | Install Command |
|---------|-----------------|
| COVID-19 | `pip install -r covid19-pandemic-analysis/requirements.txt` |
| Cracow Real Estate | `pip install -r cracow-real-estate-pricing/requirements.txt` |
| Global Terrorism (R) | See `global-terrorism-eda/requirements.txt` |
| Polar Watch | `pip install -r polar-watch-fitness-analysis/requirements.txt` |
| FX Trading | `pip install -r fx-trading-analysis/requirements.txt` |

Each project folder contains its own README with specific setup instructions.

### Running a Notebook

```bash
cd cracow-real-estate-pricing
jupyter notebook 00_Data_Wrangling.ipynb
```

---

## Repository Structure

```
datalens/
├── README.md
├── LICENSE
├── covid19-pandemic-analysis/
│   ├── data/
│   │   └── download_data.py
│   ├── features/
│   │   ├── make_all.py
│   │   ├── make_cases.py
│   │   ├── make_cases_daily_change.py
│   │   ├── make_cases_since_t0.py
│   │   ├── make_continents.py
│   │   ├── make_coordinates.py
│   │   ├── make_country_stats.py
│   │   ├── make_country_to_continent.py
│   │   ├── make_mortality.py
│   │   ├── make_world_bank.py
│   │   └── utils.py
│   ├── visualizations/
│   │   └── covid_data_viz.py
│   ├── notebooks/
│   │   ├── Data-wrangling.ipynb
│   │   ├── Exploratory-analysis-globally.ipynb
│   │   ├── Exploratory_analysis_fancy_plot.ipynb
│   │   ├── Exploratory-analysis-mortality.ipynb
│   │   └── Exploratory_analysis_socioeconomic.ipynb
│   └── tests/
├── cracow-real-estate-pricing/
│   ├── 00_Data_Wrangling.ipynb
│   ├── 01_Exploratory_Analysis.ipynb
│   ├── 02_Model.ipynb
│   └── img/
├── global-terrorism-eda/
│   ├── Global Terrorism.ipynb
│   └── img/
├── polar-watch-fitness-analysis/
│   ├── Polar.ipynb
│   ├── mdl_results.txt
│   └── img/
└── fx-trading-analysis/
    ├── Trading Results Analysis.ipynb
    └── img/
```

---

## Contributing

Contributions, issues, and feature requests are welcome.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Author

**Your Name**

- GitHub: [@your-username](https://github.com/your-username)
- LinkedIn: [your-profile](https://linkedin.com/in/your-profile)

## Acknowledgements

Based on / adapted from the original work by Sarvesh Kumar Sharma ([@shsarv](https://github.com/shsarv)). Datasets are credited to JHU CSSE, the World Bank, and the Global Terrorism Database (START, University of Maryland).
