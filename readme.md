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

[E-Commerce Presentation.pdf](https://github.com/user-attachments/files/29950291/E-Commerce.Presentation.pdf)

