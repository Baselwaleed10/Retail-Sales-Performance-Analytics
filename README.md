# Superstore Sales Data Analysis

## Overview
This repository contains `final_pro.ipynb`, an end-to-end exploratory data analysis (EDA) and time-series exploration of the popular **Superstore** retail dataset. The notebook walks through loading the raw CSV, cleaning and preprocessing the data, uncovering patterns with visual analytics, and extracting actionable insights for business decision-making.

## Dataset
The analysis uses the public *Sample - Superstore* dataset (2014-2017 United States office-supply sales). If you do not already have the CSV, download it from Tableau’s public resources or Kaggle and place it in the project root as `Superstore.csv` (or edit the notebook path accordingly).

| Column | Description |
| ------ | ----------- |
| **Order ID** | Unique order identifier |
| **Order Date** | Date the order was placed |
| **Ship Date** | Date the order shipped |
| **Customer Name** | Customer full name |
| **Segment** | Consumer / Corporate / Home Office |
| **City**, **State**, **Postal Code**, **Region** | Shipping geography |
| **Category**, **Sub-Category** | Product taxonomy |
| **Sales**, **Quantity**, **Discount**, **Profit** | Financial metrics |

*(See the notebook for the full data dictionary.)*

## Environment
```bash
python>=3.9
pandas
numpy
matplotlib
seaborn
plotly
nbformat
```
You can install everything at once:
```bash
pip install -r requirements.txt
```
*(Create a `requirements.txt` with the packages above or use your own virtual-env manager such as Poetry or Conda.)*

## Running the notebook
```bash
jupyter notebook final_pro.ipynb
```
Follow the cells top-to-bottom. Each major section is numbered and described in markdown headers:
1. **Load the data** – read CSV into a DataFrame
2. **Basic exploration** – shape, types, null counts, sample rows
3. **Data preprocessing** – handle missing postal codes, drop duplicates, convert dtypes
4. **Exploratory Data Analysis**  
   • Distribution plots (sales, profit)  
   • Category & sub-category breakdowns  
   • Correlation heatmap of numeric features
5. **Time-Series Analysis** – resample monthly sales, visualize trends & seasonality
6. **Insights & Conclusions** – markdown bullet summary of key findings

## Key findings (spoilers!)
* **Up-trend** in sales from mid-2019 through the end of 2020.
* *Technology* is the highest-revenue category; *Chairs* and *Phones* dominate sub-categories.
* **Seasonality**: noticeable November–December sales spikes reflecting holiday demand.
* Strong positive correlation between *Sales* and *Profit*; discounts erode profitability beyond ~20 %.

See the notebook for detailed visuals and commentary.

## Repository structure
```
.
├── final_pro.ipynb       # Jupyter notebook with full analysis
├── Superstore.csv        # Raw data (add yourself)
└── README.md             # You are here 📄
```

## Next steps / ideas
* Extend forecasting with ARIMA / Prophet to predict 2021-2022 sales.
* Build an interactive dashboard (Plotly Dash or Tableau) for stakeholders.
* Apply clustering to segment customers by buying behavior.

---
Made with ❤️ and Python.
