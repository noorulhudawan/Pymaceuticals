# Pymaceuticals Inc. — Tumor Response to Treatment

A data analysis project exploring the results of a pre-clinical study on 249 mice testing the efficacy of Pymaceuticals' lead drug candidate, **Capomulin**, against 9 other treatment regimens for squamous cell carcinoma (SCC), a form of skin cancer.

The analysis uses **pandas**, **Matplotlib**, and **scipy** to clean, summarize, and visualize tumor volume data across drug regimens, then examines the relationship between mouse weight and tumor volume for the Capomulin regimen.

## Project Structure

```
├── data/
│   ├── Mouse_metadata.csv        # Mouse ID, drug regimen, sex, age, weight
│   └── Study_results.csv         # Mouse ID, timepoint, tumor volume, metastatic sites
├── pymaceuticals_starter.ipynb   # Main analysis notebook
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook or JupyterLab

### Installation

```bash
git clone <repo-url>
cd pymaceuticals
pip install pandas matplotlib scipy jupyter
jupyter notebook pymaceuticals_starter.ipynb
```

## Analysis Overview

1. **Data Preparation** — Merge mouse metadata with study results; identify and remove a duplicate mouse (`g989`) with conflicting Timepoint records, leaving a clean dataset of 248 mice.
2. **Summary Statistics** — Mean, median, variance, standard deviation, and SEM of tumor volume for each of the 10 drug regimens.
3. **Bar & Pie Charts** — Number of observed timepoints per regimen, and the sex distribution of study mice.
4. **Quartiles & Outliers** — IQR-based outlier detection and a box plot comparing final tumor volume across Capomulin, Ramicane, Infubinol, and Ceftamin.
5. **Line & Scatter Plots** — Tumor volume over time for a single Capomulin-treated mouse, and average tumor volume vs. mouse weight across the Capomulin regimen.
6. **Correlation & Regression** — Pearson correlation coefficient and linear regression between mouse weight and average tumor volume.

## Key Findings

- **Capomulin and Ramicane were the most effective regimens**, producing the lowest mean/median final tumor volumes (~40 mm³) with the least variability, compared to ~52–55 mm³ for the other eight regimens.
- **Weight correlates strongly with tumor volume** within the Capomulin group (Pearson r = 0.84) — heavier mice tended to have larger tumors.
- **Outliers were rare**: only one potential outlier was found (in the Infubinol regimen) across the four regimens examined in detail.
- The study population was **balanced by sex** (~51% male / ~49% female), so sex is not a likely confounder.

## Built With

- [pandas](https://pandas.pydata.org/) – data cleaning and aggregation
- [Matplotlib](https://matplotlib.org/) – data visualization
- [SciPy](https://scipy.org/) – statistical tests and linear regression

## License

This project is for educational purposes as part of a data analysis coursework module.
