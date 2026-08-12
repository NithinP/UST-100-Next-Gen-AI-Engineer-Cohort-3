# Assignment 1 — Zomato Restaurant Data Analysis

Exploratory Data Analysis (EDA) on the Zomato restaurant dataset using Pandas, NumPy, Matplotlib, and Seaborn.

## Files

- `Zomato_Data_Analysis.ipynb` — the analysis notebook (Colab-ready; loads from `/content/test_zomato.csv`).
- `UST_Assignment1_Zomato_Report.pdf` — documentation report (overview, cleaning, analysis, visualizations, conclusion).
- `test_zomato.csv` — the dataset (9,551 restaurants).
- `charts/` — exported visualizations.

## How to run

1. Open `Zomato_Data_Analysis.ipynb` in Google Colab.
2. Upload `test_zomato.csv` to the session (it will sit at `/content/`).
3. Runtime → Run all.

## Key findings

- 141 unique cities; **New Delhi** has the most restaurants (5,473) — the Delhi NCR region dominates.
- **North Indian** is the most common cuisine, followed by Chinese and Fast Food.
- Average rating ≈ **3.44** (rated restaurants only; rating 0 = "Not rated").
- Most-voted restaurant: **Toit, Bangalore** (10,934 votes).
- Table-booking restaurants rate slightly higher; online delivery shows no real rating advantage once unrated restaurants are excluded.
- Average rating rises steadily with price range.
