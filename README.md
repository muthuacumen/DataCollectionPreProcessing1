# Lab 01: Data Collection and Preprocessing

## Objective

Demonstrate fundamental data collection and preprocessing techniques using Python and pandas, including:
- Loading and inspecting CSV data
- Designing custom data structures (Transaction class)
- Data cleaning and transformation
- Feature engineering
- Aggregation and serialization

## Dataset

**Source:** [Retail Transactions Dataset](https://www.kaggle.com/datasets/prasad22/retail-transactions-dataset) (Kaggle)

| File | Description | Records |
|------|-------------|---------|
| `Retail_Transactions_Dataset.csv` | Raw e-commerce transactions | 50,000 |
| `cleaned_transactions.csv` | Cleaned output (CSV) | 50,000 |
| `cleaned_transactions.json` | Cleaned output (JSON) | 50,000 |

### Fields

| Column | Type | Description |
|--------|------|-------------|
| Transaction_ID | string | Unique identifier |
| Date | string | Purchase date |
| Customer_Name | string | Customer name |
| Product | string | Product purchased |
| Total_Items | int | Quantity |
| Total_Cost | float | Transaction amount (USD) |
| City | string | Shipping city |
| Promotion | string | Coupon/promo code |

## Setup

### Prerequisites
- Python 3.10+
- Jupyter Notebook or JupyterLab

### Installation

```bash
# Clone the repository
git clone <repo-url>
cd DataCollectionPreprocessing1

# Create virtual environment
python -m venv .venv

# Activate (Windows)
.venv\Scripts\activate

# Activate (macOS/Linux)
source .venv/bin/activate

# Install dependencies
pip install pandas ipykernel

# Register Jupyter kernel
python -m ipykernel install --user --name=lab01_venv --display-name="Python (Lab01)"
```

### Run the Notebook

```bash
jupyter notebook lab01_data_collection_preprocessing.ipynb
```

Select kernel: **Python (Lab01)**

## Contents

| Step | Description |
|------|-------------|
| 1 | Load dataset and preview |
| 2 | Data structure choice (DataFrame justification) |
| 3 | Transaction class with `clean()` and `total()` |
| 4 | Bulk load CSV to Transaction objects |
| 5 | Data profiling (min/mean/max price, unique cities) |
| 6 | Identify dirty data (missing, duplicates, invalid) |
| 7 | Cleaning rules with before/after comparison |
| 8 | Transform coupon codes using regex |
| 9 | Feature engineering (`days_since_purchase` property) |
| 10 | Aggregation (revenue per city) |
| 11 | Serialization (save to CSV and JSON) |
| 12 | Reflection on functions vs methods |

## Project Structure

```
DataCollectionPreprocessing1/
├── data/
│   ├── Retail_Transactions_Dataset.csv   # Raw data
│   ├── cleaned_transactions.csv          # Output (after running notebook)
│   └── cleaned_transactions.json         # Output (after running notebook)
├── lab01_data_collection_preprocessing.ipynb
├── README.md
├── .gitignore
└── .venv/                                # Virtual environment (not tracked)
```

## Key Concepts Demonstrated

- **OOP**: Transaction class with encapsulation
- **Data Cleaning**: String normalization, type conversion, handling nulls
- **Regex**: Extracting numeric values from promotion codes
- **Properties**: `@property` decorator for computed fields
- **Serialization**: CSV and JSON export

## Author

Data Collection and Preprocessing Lab
Python Data Engineering Course
