# Web-Scraped Grocery Pricing Pipeline & Unsupervised Market Segmentation

**Project Overview: Real-Time Freshco Competitor Intelligence Pipeline**

Built an automated, end-to-end data engineering and machine learning pipeline that orchestrates the daily ingestion of live, web-scraped grocery data from Freshco’s production site. The system systematically resolves business-critical pricing errors, extracts structured product attributes from unstructured text, and dynamically segments inventory using unsupervised machine learning.

- Detailed Pipeline Architecture
1. Live Web Ingestion & Orchestration
The Process: Designed a dynamic web-scraping layer configured to simulate real-time user requests across Freshco's live digital storefront.

The Output: Automates daily extraction of localized, live product titles, categories, structural pricing details, and active promotional banners, pipe-lining raw data instantly into the processing engine.

2. Defensive Data Quality Engineering (Price Audit)
The Challenge: Real-time web-scraped data frequently contains "dirty" rows caused by UI structural changes or misconfigured store promotions. A major anomaly detected was inverted pricing labels—where a temporary promotional "Sale Price" was erroneously captured as higher than the "Regular Price".

The Solution: Programmed an automated auditing layer that flags these integrity violations, cross-references historical pricing baselines, and programmatically flips or cleans the values to safeguard downstream financial analytics.

3. Regex Feature Extraction Engine
The Challenge: Essential e-commerce product fields (like pack sizes or exact item volumes) are often trapped inside unstructured, messy product description strings (e.g., "Freshco Choice Bananas 5pk 1.5kg").

The Solution: Engineered a robust Regular Expression (Regex) extraction module. This layer parses raw strings on-the-fly, decomposing chaos into clean, analytics-ready schema attributes: Pack_Quantity and Unit_Size.

4. Unsupervised Product Tiering (K-Means Clustering)
The Machine Learning Layer: Fed the standardized, real-time dataset into a K-Means Clustering model to uncover hidden pricing strategies and structural value segments across Freshco's inventory.

The Segments: The algorithm mathematically grouped the scraped catalog into three distinct competitor value tiers:

🟢 Budget Segment ($0–$10): High-volume everyday essentials.

🔵 Mid-Tier Segment ($10–$20): Standard pantry staples and family-sized items.

🔴 Premium/Bulk Segment ($20+): High-value meats, specialty imports, and bulk packaging.

Outlier Detection: The model effectively isolated anomalous promotional data points—highlighting products with extreme, aggressive discount margins relative to their baseline cluster peers.

📈 Tangible Business Value
Real-Time Market Visibility: Empowers retail decision-makers to track competitor price movements, spot flash-sales instantly, and optimize dynamic pricing models using live market data rather than stale, historical datasets.

Downstream Readiness: The pipeline delivers a clean, structurally sound, feature-rich dataset fully optimized to feed predictive forecasting models, supply chain demand algorithms, or competitive pricing engines.

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

