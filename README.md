# E-Commerce Sales Performance & Smart Pricing Insights

> **IBM SkillsBuild Data Analytics with AI — Academic Internship Program**
> *Conducted by BharatCares in association with AICTE*

| Field | Details |
|---|---|
| **Intern Name** | Nikita Thakur |
| **Institution** | Oriental University Indore |
| **Specialization** | MCA (AIML) |
| **Project Title** | E-Commerce Sales Performance & Smart Pricing Insights |
| **Dataset** | Unlock Profits with E-Commerce Sales Data (Kaggle) |

---

## 📁 Repository Structure

```
├── NikitaThakur_ECommerce_Smart_Pricing.ipynb   # Full analysis notebook
├── app.py                                        # Streamlit interactive dashboard
├── NikitaThakur_ProjectReport.docx              # Academic project report
├── requirements.txt                              # Python dependencies
└── README.md                                     # This file
```

---

## 📦 Dataset

| | |
|---|---|
| **Source** | [Kaggle — Unlock Profits with E-Commerce Sales Data](https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data) |
| **Rows** | ~2,000 transactions (synthetic representative sample included) |
| **Key Columns** | `category`, `sub_category`, `region`, `actual_price`, `selling_price`, `discount_pct`, `units_sold`, `rating`, `rating_count` |

To use the real Kaggle dataset, download and place the CSV in the project root, then replace the data-generation block in the notebook with:
```python
df = pd.read_csv("your_dataset.csv")
```

---

## 🛠️ Technology Stack

| Layer | Tools |
|---|---|
| Language | Python 3.10+ |
| Data Wrangling | pandas, numpy |
| Visualisation | matplotlib, seaborn, plotly |
| Machine Learning | scikit-learn (LinearRegression, RandomForestRegressor) |
| Interactive Dashboard | Streamlit |
| Notebook Environment | Jupyter |

---

## ⚙️ Setup & Run Instructions

### 1 · Clone / download the repository

```bash
git clone https://github.com/<your-username>/ecommerce-smart-pricing.git
cd ecommerce-smart-pricing
```

### 2 · Create a virtual environment (recommended)

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
```

### 3 · Install dependencies

```bash
pip install -r requirements.txt
```

### 4 · Run the Jupyter Notebook

```bash
jupyter notebook NikitaThakur_ECommerce_Smart_Pricing.ipynb
```

Run all cells top-to-bottom. Output charts are saved as `fig_*.png` in the working directory.

### 5 · Launch the Streamlit Dashboard

```bash
streamlit run app.py
```

The app opens automatically at `http://localhost:8501`.

---

## 🔍 Key Business Findings

### 1 · Revenue Drivers
- **Units Sold** and **Selling Price** are the two strongest predictors of gross revenue (confirmed by Random Forest feature importances).
- Electronics and Home & Kitchen categories generate the highest cumulative revenue.

### 2 · Discount Impact
- Products in the **Low-to-Moderate discount band (0–25%)** consistently show the highest **Revenue Efficiency** — the ratio of actual revenue to potential revenue.
- Aggressive discounting (>45%) degrades revenue efficiency faster than it compensates with volume uplift.

### 3 · Regional Insights
- Revenue distribution across North / South / East / West regions is relatively uniform, suggesting pricing strategies should be driven by **category and price band** rather than region.

### 4 · ML Model Performance

| Model | MAE | RMSE | R² |
|---|---|---|---|
| Linear Regression | Higher | Higher | Lower |
| **Random Forest** | **Lower ✅** | **Lower ✅** | **Higher ✅** |

Random Forest captures non-linear interactions between price, discount, and volume that Linear Regression cannot model linearly.

### 5 · Smart Pricing Recommendation
Set category-specific discount ceilings (≤25% for Electronics and Fashion; ≤15% for Books) to maximise revenue efficiency while remaining competitive.

---

## 📊 Dashboard Features
- **Sidebar filters** — Category, Region, Price Band, Discount % Range
- **Live KPI cards** — Total Revenue, Orders, Avg Discount, Revenue Efficiency, Discount Loss
- **Interactive charts** — Revenue by category, Discount distribution, Regional heatmap, Scatter analysis
- **ML comparison panel** — Side-by-side model metrics and feature importances
- **Smart Pricing Simulator** — Real-time revenue/loss curves across discount levels

---

## 📄 License

This project is submitted for academic evaluation under the IBM SkillsBuild × BharatCares × AICTE internship program. All rights reserved to Nikita Thakur, Oriental University Indore.

---

*Made with ❤️ and Python · IBM SkillsBuild 2025*
