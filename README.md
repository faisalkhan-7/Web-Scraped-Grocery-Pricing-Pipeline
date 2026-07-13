# Web-Scraped-Grocery-Pricing-Pipeline
This project establishes an end-to-end data engineering and data science pipeline that ingests a messy grocery dataset of 250 items, enforces schema integrity, extracts buried categorical dimensions, and applies unsupervised machine learning to segment inventory profiles.
# Web-Scraped Grocery Pricing Pipeline & Unsupervised Market Segmentation

An end-to-end data engineering and machine learning pipeline that ingests raw, messy e-commerce grocery data, resolves pricing structural errors, extracts hidden categorical features, and clusters products into value segments.

## 📁 Repository Structure
```text
├── data/
│   ├── raw/                      # Original web-scraped messy data (JSON/CSV)
│   └── processed/                # Cleaned datasets with extracted features
├── notebooks/
│   └── grocery_eda_and_ml.ipynb  # Main Google Colab / Jupyter notebook
├── src/
│   ├── data_cleaning.py          # Data cleaning & regex extraction functions
│   ├── eda_visualizations.py     # Script to generate Seaborn charts
│   └── price_clustering.py       # K-Means machine learning modeling logic
├── output/
│   └── figures/                  # Saved .png images of the visualizations
├── .gitignore
├── requirements.txt              # Required python packages
└── README.md                     # Project summary and documentation
