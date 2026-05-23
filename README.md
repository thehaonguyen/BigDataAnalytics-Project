# Big Data Analytics — Project 1
## Analyzing Sales Data with Dask

---

## Overview

This project demonstrates scalable data analysis using **Dask**, a parallel computing library in Python. The analysis is performed on the [Sample Sales Dataset](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data) (2,823 rows × 25 columns), covering the full pipeline from data cleaning through machine learning, performance optimization, and reporting.

---

## Dataset

| Property | Value |
|---|---|
| Source | [Kaggle — Sample Sales Data](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data) |
| File | `sales_data_sample.csv` |
| Size | 2,823 rows × 25 columns |
| Encoding | Latin-1 |
| Key columns | SALES, QUANTITYORDERED, PRICEEACH, MSRP, PRODUCTLINE, CUSTOMERNAME, ORDERDATE, COUNTRY, DEALSIZE |

> Download the dataset from Kaggle and place it at `data/sales_data_sample.csv` before running the notebook.

---

## Project Structure
BigDataAnalytics_Project/
├── data/
│   └── sales_data_sample.csv           # Raw dataset (download from Kaggle)
├── output/
│   ├── BigDataAnalytics_Project.pdf    # Main Jupyter Notebook (PDF format)
│   └── sales_dashboard.png             # Dashboard visualization of the data
├── .gitignore                          # Configuration file to exclude files/folders from Git commits
├── BigDataAnalytics_Project.ipynb      # Main Jupyter Notebook
├── LICENSE                             # Project license
├── requirements.txt                    # Python dependencies
└── README.md                           # This file
---

## Tasks Covered

| Task | Description |
|---|---|
| **Task 1 — Data Preparation** | Load with Dask, handle missing values, detect and treat outliers, check inconsistencies |
| **Task 2 — EDA** | Summary statistics, sales distribution by product/customer/time/country, deal size analysis |
| **Task 3 — Feature Engineering** | Customer spending, avg sales per product, time features (quarter, day of week, weekend), revenue per unit, discount ratio |
| **Task 4 — Advanced Analytics** | K-Means customer segmentation (RFM), Random Forest + Gradient Boosting forecasting, Apriori association rule mining |
| **Task 5 — Performance Optimization** | Partition size tuning, lazy evaluation, memory comparison (Pandas vs Dask), scheduler benchmarking (synchronous / threaded / distributed) |
| **Task 6 — Reporting** | 9-panel analytics dashboard, key findings summary, business recommendations |

---

## Installation

### 1. Clone or download this repository

```bash
git clone https://github.com/your-username/BigDataAnalytics_Project.git
cd BigDataAnalytics_Project
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate        # macOS / Linux
venv\Scripts\activate           # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Download the dataset

Download `sales_data_sample.csv` from [Kaggle](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data) and place it inside the `data/` folder:
data/sales_data_sample.csv
### 5. Launch the notebook

```bash
jupyter notebook BigDataAnalytics_Project.ipynb
```

---

## Key Findings

| Section | Finding |
|---|---|
| **Top Product Line** | Classic Cars generate the highest total revenue across all years |
| **Peak Season** | Q4 (October–November) consistently peaks; Q1 is the weakest quarter |
| **Top Market** | USA dominates total sales, followed by Spain and France |
| **Top Customers** | Euro Shopping Channel and Mini Gifts Distributors Ltd are the highest spenders |
| **Customer Segments** | K-Means identified High-Value, Mid-Value, and Low-Value clusters plus a VIP outlier group |
| **Best ML Model** | Random Forest outperformed Gradient Boosting (lower MAE and RMSE, higher R²) |
| **Dask Optimization** | Lazy loading saved significant RAM vs Pandas; distributed scheduler scaled across all CPU cores |

---

## Business Recommendations

1. **Prioritize Classic Cars** — highest revenue-generating product line
2. **Launch Q3 promotions** — build momentum heading into the Q4 peak
3. **Loyalty programs for High-Value and VIP segments** — they drive disproportionate revenue
4. **Cross-sell bundles** — based on frequently co-purchased product lines from association rules
5. **Expand in USA, Spain, and France** — top three revenue markets
6. **Negotiate volume pricing on Medium deals** — largest order share but lower value per transaction than Large deals
7. **Apply discounts strategically** — Discount Ratio was a significant predictor of order quantity

---

## Tools and Libraries

| Library | Purpose |
|---|---|
| `dask` | Parallel and distributed DataFrame processing |
| `distributed` | Dask distributed scheduler and local cluster |
| `pandas` | Data manipulation and pandas interoperability |
| `numpy` | Numerical operations |
| `matplotlib` | Charts and dashboard visualizations |
| `seaborn` | Statistical visualizations |
| `scikit-learn` | K-Means clustering, Random Forest, Gradient Boosting, preprocessing |
| `mlxtend` | Apriori algorithm and association rule mining |
| `statsmodels` | Time series decomposition |
| `psutil` | Memory usage measurement for optimization benchmarks |

---

## Requirements

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Minimum 4 GB RAM recommended (Task 5 creates a large synthetic dataset of ~1.4M rows for benchmarking)

---

## Team Members

| Name | Student ID | Responsibility |
|---|---|---|
| Nguyễn Thế Hào | ITDSIU22139 |
| Phạm Nguyễn Công Danh | ITDSIU23035 |
| Đỗ Thanh Bảo Anh | ITDSIU22175 |
| Cao Bảo Khương | ITDSIU22176 |
| Nguyễn Thiện Quân | ITDSIU23020 |


---

## Course Information

| Field | Value |
|---|---|
| Course | Big Data Analytics |
| Institution | International University - Vietnam National University Ho Chi Minh City |
| Instructor | Mai Hoàng Bảo Ân |
| Semester | Semester 2 / Year 2025-2026 |