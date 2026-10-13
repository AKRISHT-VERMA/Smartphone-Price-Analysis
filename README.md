# Smartphone Price Analysis

An end-to-end data analysis project exploring smartphone specifications and their relationship with price. The workflow covers web scraping, data cleaning, exploratory data analysis (EDA), and feature engineering for future machine-learning price prediction.

## Project workflow

1. **Data collection** — `Notebooks/adv_web_scrapping.ipynb` contains the web-scraping work.
2. **Data cleaning** — `Notebooks/Data cleaning Smartphone.ipynb` transforms the raw specification data into structured columns.
3. **Exploratory data analysis** — `Notebooks/EDA_Smartphone_Enhanced.ipynb` explores price distributions, specification relationships, and correlations.
4. **Feature engineering** — `Datasets/Smartphones_Feature_Engineered.csv` contains additional display and specification features, including resolution dimensions, resolution category, PPI, aspect ratio, camera count, battery tier, and refresh-rate tier.

## Repository structure

```text
Smartphone/
├── Datasets/
│   ├── smartphones.csv
│   ├── smartphones_cleaned.csv
│   └── Smartphones_Feature_Engineered.csv
├── Notebooks/
│   ├── adv_web_scrapping.ipynb
│   ├── Data cleaning Smartphone.ipynb
│   └── EDA_Smartphone_Enhanced.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Setup

Use Python 3.10 or newer, create a virtual environment, and install the dependencies:

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Open the notebooks in VS Code or Jupyter. If a notebook refers to a local absolute path, update it to a relative path such as `../Datasets/smartphones.csv` or `../Datasets/smartphones_cleaned.csv`, depending on the notebook's location.

## Dataset files

- `smartphones.csv` — raw collected smartphone data.
- `smartphones_cleaned.csv` — structured and cleaned smartphone data.
- `Smartphones_Feature_Engineered.csv` — data with additional engineered features.

## Notes and limitations

- Smartphone prices and specifications may change over time and may vary by seller or configuration.
- Some values may have been imputed. Treat imputed values as estimates rather than verified specifications.
- Correlation does not imply causation. Correlation results are exploratory and should not be interpreted as proof that a feature causes a higher or lower price.
- Before machine-learning training, inspect missing values, prevent target leakage, encode categorical variables, and evaluate models on a held-out test set.

## Future work

- Build and evaluate regression models for smartphone price prediction.
- Compare feature sets and model performance using a held-out test set.
- Improve validation of imputed specifications and document data-source limitations.
