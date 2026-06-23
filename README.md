# 🌍 World Happiness Report 2021 - Exploratory Data Analysis

A mini data analysis project exploring the World Happiness Report 2021 dataset (`world-happiness-report-2021.csv`) using `pandas`, `numpy`, and `matplotlib`. The notebook walks through data loading, ranked country analysis, correlation study, regional grouping, and visualization.

## Project Structure

```
.
├── notebook.ipynb                      # Main notebook
├── world-happiness-report-2021.csv     # Dataset (must be placed in the same directory)
└── README.md
```

## Requirements

* Google Colab (recommended), or Jupyter Notebook / JupyterLab locally
* Python 3.x
* pandas
* numpy
* matplotlib

These libraries come pre-installed on Google Colab, so no setup is needed there. For local use, install with:

```
pip install pandas numpy matplotlib jupyter
```

## Dataset

The notebook expects a `world-happiness-report-2021.csv` file (the World Happiness Report 2021 dataset with columns such as `Country name`, `Regional indicator`, `Ladder score`, `Logged GDP per capita`, `Social support`, `Healthy life expectancy`, `Freedom to make life choices`, `Generosity`, `Perceptions of corruption`, etc.).

On Colab: upload `world-happiness-report-2021.csv` to the session via the Files panel (left sidebar → Upload), or mount Google Drive and point `pd.read_csv()` to the file's path there. Files uploaded directly to the session are deleted when the runtime disconnects, so re-upload if you restart.

The dataset can be downloaded from [Kaggle — World Happiness Report 2021](https://www.kaggle.com/datasets/ajaypalsinghlo/world-happiness-report-2021).

## What the Notebook Does

1. **Data Loading & Preview**
   * Loads `world-happiness-report-2021.csv` into a DataFrame
   * Previews the first 5 rows with `.head()`

2. **Top & Bottom 10 Countries**
   * Sorts countries by `Ladder score`
   * Prints the 10 happiest and 10 least happy countries

3. **Correlation Analysis**
   * Computes Pearson correlation between `Ladder score` and all six contributing factors
   * Identifies which factors are most strongly linked to happiness

4. **GDP Statistics**
   * Calculates the mean and standard deviation of `Logged GDP per capita` using `numpy`

5. **Regional Analysis**
   * Groups countries by `Regional indicator`
   * Computes and ranks average happiness score per region

6. **Visualizations**
   * Bar chart: Top 10 happiest countries by Ladder score
   * Scatter plot: GDP per capita vs. Happiness score

## How to Run

1. Open `notebook.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Upload `world-happiness-report-2021.csv` to the Colab session (Files panel → Upload), or mount Google Drive and update the file path in the `pd.read_csv()` call.
3. Run all cells in order (Runtime → Run all).

## Key Insights

* 🏆 **Nordic countries** (Finland, Denmark, Iceland) consistently rank among the happiest nations.
* 💰 **GDP per capita** and **Social support** show the strongest positive correlation with happiness.
* 🌍 **Western Europe** and **North America & ANZ** are the happiest regions on average.
* 📉 **Sub-Saharan Africa** records the lowest regional happiness scores.
* The scatter plot confirms a clear upward trend between wealth and well-being, though notable outliers exist.

## Notes

* The `Ladder score` is based on the **Cantril ladder** — a self-reported life evaluation where respondents imagine a ladder from 0 (worst possible life) to 10 (best possible life).
* `Logged GDP per capita` values are **log-transformed**, not raw dollar figures, so they cannot be directly interpreted as income amounts.
* The correlation analysis uses **Pearson correlation**, which only captures linear relationships — some factors may have a non-linear influence on happiness.
* The dataset covers **149 countries** for 2021; countries with insufficient survey data are excluded from the report entirely.

## Open in Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nihanilufar/World-Happiness-Report/blob/main/notebook.ipynb)
