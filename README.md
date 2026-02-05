# 🏀 NBA Win Probability Model

**A machine learning system that predicts the probability of an NBA team winning at any point during a game.**

<!-- TODO: Add hero image here once generated in Phase 2 -->

## Overview

This project builds a real-time win probability model using 5 seasons of NBA play-by-play data (2020-21 through 2024-25). Given any game state (score differential, time remaining, possession, and team strength), the model outputs the probability that the home team wins.

The final product includes an **interactive Streamlit application** where users can explore win probability curves for historical games or simulate custom scenarios.

## Key Findings

*Coming soon after EDA and modeling phases.*

## Methodology
```
Raw Play-by-Play Data (nba_api)
        │
        ▼
Data Cleaning & Feature Engineering
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Model Training & Evaluation
  ├── Logistic Regression (baseline)
  └── XGBoost (advanced)
        │
        ▼
Model Interpretation (SHAP)
        │
        ▼
Interactive Streamlit App
```

## Features Used

| Feature | Description |
|---|---|
| `score_differential` | Home score minus away score |
| `seconds_remaining` | Total seconds left in regulation |
| `quarter` | Current period (1-4, 5+ for OT) |
| `home_has_possession` | Binary flag for current possession |
| `elo_differential` | Pre-game team strength difference |
| `momentum` | Scoring run in last 10 possessions |

## Model Performance

*Coming soon. Will include log loss, Brier score, and calibration curves.*

## Live App

*Coming soon. Will be deployed on Streamlit Community Cloud.*

## AI Workflow

This project was built with intentional, documented use of AI tools (primarily Claude by Anthropic). See [`AI_WORKFLOW.md`](AI_WORKFLOW.md) for a transparent breakdown of how AI was used at each phase, what decisions were made manually, and reflections on AI-assisted development.

## Project Structure
```
nba-win-probability/
├── README.md
├── AI_WORKFLOW.md
├── requirements.txt
├── data/
│   ├── raw/                  # Raw API responses
│   └── processed/            # Cleaned, model-ready data
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_eda.ipynb
│   └── 04_modeling.ipynb
├── src/
│   ├── data_pipeline.py      # API data collection
│   ├── features.py           # Feature engineering
│   └── model.py              # Model training and evaluation
├── app/
│   └── streamlit_app.py      # Interactive Streamlit app
├── tests/
│   └── test_features.py      # Unit tests
└── outputs/
    ├── figures/              # Saved visualizations
    └── models/               # Serialized trained models
```

## Setup
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/nba-win-probability.git
cd nba-win-probability

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## Tech Stack

**Data:** Python, pandas, nba_api, pyarrow
**Modeling:** scikit-learn, XGBoost, SHAP, Optuna
**Visualization:** Plotly, Matplotlib, Seaborn
**App:** Streamlit
**Infrastructure:** GitHub, pytest

## Author

**Victor** -- Data Analytics | [Portfolio](YOUR_PORTFOLIO_URL) | [LinkedIn](YOUR_LINKEDIN_URL)

## License

MIT License
