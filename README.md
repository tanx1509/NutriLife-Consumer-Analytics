text ██╗   ██╗██████╗  █████╗  █████╗ ███╗   ██╗ ██║   ██║██╔══██╗██╔══██╗██╔══██╗████╗  ██║ ██║   ██║██████╔╝███████║███████║██╔██╗ ██║ ██║   ██║██╔══██╗██╔══██║██╔══██║██║╚██╗██║ ╚██████╔╝██║  ██║██║  ██║██║  ██║██║ ╚████║  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝ 

Proxy Wealth Detection System | Project UDAAN

Income lies. Spending patterns don’t. This system identifies high-value customers where traditional financial signals fail.

---

## The Problem, Precisely

In many financial systems, income is the primary signal for creditworthiness.

It is also:
- misreported  
- unavailable  
- unreliable  

text Observed:   High-income individuals not captured   Low-income proxies receiving misclassification   Large segment of “invisible high-value users”  Result:   Poor targeting   Inefficient credit allocation   Missed high-LTV customers 

The system does not fail due to lack of data.  
It fails due to wrong signals.

---

## The Solution

UDAAN reframes the problem:

👉 Not “Who earns more?”  
👉 But “Who behaves like a high-value customer?”

It builds a proxy-based prediction system that:
- bypasses unreliable income data  
- leverages behavioral and transactional patterns  
- translates predictions into deployable field logic  

---

## System Architecture

text Raw Household Data (~50,000 records)         │         ▼ ┌──────────────────────────────────┐ │ Feature Engineering              │ │ • Consumption patterns           │ │ • Transaction behavior           │ │ • Location-based proxies         │ │ • Retail interaction signals     │ └──────────────────────────────────┘         │         ▼ ┌──────────────────────────────────┐ │ Gradient Boosting Model          │ │ (LightGBM / XGBoost)             │ │                                  │ │ Output: Probability of           │ │ High-Value Customer              │ └──────────────────────────────────┘         │         ▼ ┌──────────────────────────────────┐ │ Model Validation                 │ │ • Cross-validation               │ │ • AUC ≈ 0.92                     │ │ • Stability checks               │ └──────────────────────────────────┘         │         ▼ ┌──────────────────────────────────┐ │ Deployment Layer                 │ │ • Retailer-level proxy signals   │ │ • Field-friendly indicators      │ │ • No reliance on income data     │ └──────────────────────────────────┘ 

---

## Core Metrics

| Metric | Value |
|------|------|
| Dataset | ~50,000 households |
| Model | Gradient Boosting |
| Performance | AUC ≈ 0.92 |
| Target | High-value customer detection |
| Outcome | 150% improvement in targeting precision |

---

## Key Insights

### 1. Income is a weak signal
text Reported income does not correlate strongly with actual spending behavior → leads to systematic misclassification 

---

### 2. Behavioral proxies outperform financial inputs
text Transaction patterns + consumption behavior → significantly stronger predictive power 

---

### 3. Deployment is the real constraint
text Models are useless if they cannot be used in the field  Solution:   Convert features → retailer-observable proxies 

---

## The Deployment Insight

text Constraint:   Field agents cannot access income data  Approach:   Replace hidden variables with observable proxies  Example:   Instead of income → retail purchase behavior   Instead of assets → frequency + basket size 

👉 This transforms the model from:
Prediction → Execution-ready system

---

## Business Impact

- Identified previously invisible high-value segments  
- Improved targeting efficiency by 150%  
- Reduced dependency on unreliable income data  
- Enabled real-world deployment without infrastructure overhaul  

---

## Tech Stack

- Python (Pandas, NumPy)  
- LightGBM / XGBoost  
- Feature Engineering  
- Model Validation  

---

## Key Insight

Financial systems don’t fail because of lack of data.  
They fail because they rely on the wrong variables.

---

## Repository Structure

text udaan-proxy-wealth-detection/ │ ├── notebooks/ │   └── UDAAN_Analysis.ipynb │ ├── data/ │   └── dataset.csv │ ├── outputs/ │   └── predictions.csv │ └── README.md 

---

## Running It

Colab (recommended):
text File → Open notebook → GitHub → paste repo link Run all cells 

Local:
bash git clone https://github.com/tanx1509/udaan-proxy-wealth-detection cd udaan-proxy-wealth-detection pip install pandas numpy scikit-learn lightgbm xgboost jupyter notebook UDAAN_Analysis.ipynb 

---

Built by Tanishq Sethi
```
