# Seasonal_Agriculture_Performance_Data_Analytics-VOIS-Project
# 🌾 Seasonal Agriculture Performance Analysis

### Major Data Analytics Project — VOIS AICTE Internship Batch1 2026–2027

A complete, end-to-end data analytics study of a seasonal agriculture dataset — investigating how farming performance (yield, profit, water efficiency and risk) changes across **Kharif, Rabi and Zaid** seasons, and why.

**Author:** Om Rajendrakumar Koli

**Domain:** Agriculture Data Analytics Internship

**Tools:** Python · Pandas · NumPy · Matplotlib · Seaborn

---

## 📌 Project Goal

Agricultural performance is shaped by season — but raw farm data doesn't explain *how* or *why* on its own. This project cleans, explores and analyzes 4,000 seasonal farm records to uncover meaningful seasonal patterns, trends and relationships, and to turn those patterns into evidence-based insights and recommendations for seasonal agricultural planning.

## 📖 Problem Statement

Agricultural activities are influenced by seasonal variations in environmental conditions, farming practices, resource availability and market conditions, so performance may differ from one season to another. Raw agricultural data does not, on its own, make these seasonal differences clear. This project analyzes the dataset to identify meaningful patterns, trends, relationships and variations in performance across seasons.

## 🗂️ Dataset

`seasonal_agriculture_performance_dataset.csv` — **4,000 farm records** across Kharif, Rabi and Zaid seasons, multiple Indian states, crops and irrigation methods.

| Category | Columns |
|---|---|
| Identifiers / Location | `Farm_ID`, `State`, `District` |
| Farming practice | `Crop`, `Season`, `Farm_Area_Hectares`, `Irrigation_Method`, `Seed_Quality_Score` |
| Environmental conditions | `Rainfall_mm`, `Avg_Temperature_C`, `Humidity_pct`, `Sunlight_Hours_Day`, `Soil_pH`, `Soil_Moisture_pct` |
| Inputs / resources | `Nitrogen_kg_ha`, `Phosphorus_kg_ha`, `Potassium_kg_ha`, `Fertilizer_kg_ha`, `Pesticide_Litre_ha`, `Water_Used_m3`, `Water_Efficiency_t_per_1000m3` |
| Production & yield | `Yield_Tonnes_Ha`, `Production_Tonnes` |
| Economics | `Market_Price_INR_Tonne`, `Total_Cost_INR`, `Revenue_INR`, `Profit_INR` |
| Risk | `Disease_Pest_Risk_pct` |

## 🛠️ Workflow

The notebook (`Seasonal_Agriculture_Performance_Analysis.ipynb`) follows an end-to-end analytics workflow:

1. **Data understanding** — shape, dtypes, unique values in categorical columns
2. **Data cleaning** — missing-value imputation (group-wise median, by season/crop), duplicate check, dtype verification, IQR-based outlier investigation
3. **Descriptive & statistical analysis** — overall and season-wise summary statistics
4. **Univariate analysis** — distributions of key numeric and categorical variables
5. **Bivariate analysis** — season vs. yield/profit, rainfall vs. yield, irrigation method vs. yield
6. **Multivariate analysis** — season × crop and season × irrigation heatmaps, pairwise relationships
7. **Correlation analysis** — full numeric correlation matrix, top drivers of yield and profit
8. **Seasonal comparison summary** — yield, profit, cost, water efficiency and disease risk by season
9. **Four original student-designed analytical questions** (see below)
10. **Key insights & final conclusion** with data-driven recommendations

## ❓ Student-Designed Analytical Questions

1. **Does irrigation method affect profitability, and does the best method change by season?**
   Drip irrigation is the most profitable method in every season, and it's the *only* method still profitable on average in Zaid.
2. **Is disease/pest risk related to yield, and does that differ by season?**
   Despite Kharif having the highest average risk, risk and yield are essentially uncorrelated at the individual-farm level (r ≈ −0.03 to 0.04) — risk is a season-wide pattern, not a farm-level yield predictor.
3. **Which state has the best water efficiency in each season — is there a consistent leader?**
   No. The leader changes by season (Gujarat in Kharif, Punjab in Rabi, Karnataka in Zaid), pointing to season-specific regional conditions rather than a fixed state advantage.
4. **Do higher fertilizer/pesticide inputs translate into higher yield?**
   No — both show essentially zero correlation with yield; crop type and water efficiency are far stronger drivers.

## 💡 Key Insights

- **Kharif consistently outperforms Rabi, which outperforms Zaid** across yield, profit and water efficiency — Zaid shows a *negative* average profit.
- This seasonal ordering holds across almost every crop and irrigation method — it's a genuine seasonal effect, not driven by one crop.
- Kharif's higher output comes with a trade-off: it also has the highest disease/pest risk.
- **Water efficiency and irrigation method (especially Drip)** matter far more to profitability than raw fertilizer/pesticide input levels.
- Sugarcane operates on an entirely different yield scale from every other crop in the dataset.

## 📁 Repository Structure

```
├── Seasonal_Agriculture_Performance_Analysis.ipynb   # Full analysis notebook
├── seasonal_agriculture_performance_dataset.csv       # Dataset (4,000 records)
├── Major_Project_Seasonal_Agriculture_Performance_Analysis_.pdf  # Project brief
├── VOIS_Major_Project_PPT_Submission_Template.pptx    # Project presentation
└── README.md
```

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/Seasonal_Agriculture_Performance_Data_Analytics-VOIS-Project.git
   cd Seasonal_Agriculture_Performance_Data_Analytics-VOIS-Project
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. Open `Seasonal_Agriculture_Performance_Analysis.ipynb` in Jupyter Notebook or Google Colab.
4. If running in Colab, upload `seasonal_agriculture_performance_dataset.csv` to `/content/` (or update `file_path` in the notebook to match your dataset location).
5. Run all cells in order.

## 🧰 Technology Used

- **Python 3** (Google Colab / Jupyter Notebook)
- **Pandas & NumPy** — data cleaning and analysis
- **Matplotlib & Seaborn** — data visualization
- **Statistical methods** — IQR outlier detection, correlation analysis
- **GitHub** — version control and submission

## ✅ Project Status

Complete — data cleaning, univariate/bivariate/multivariate analysis, correlation analysis, four original analytical questions, key insights and final conclusion are all done in the notebook.

## 📜 License

This project was created as part of the **VOIS for Tech AICTE Internship (Batch1 2026–2027)** for educational purposes.
