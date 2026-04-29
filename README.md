```markdown
```text
 ██╗   ██╗██████╗  █████╗  █████╗ ███╗   ██╗
 ██║   ██║██╔══██╗██╔══██╗██╔══██╗████╗  ██║
 ██║   ██║██████╔╝███████║███████║██╔██╗ ██║
 ██║   ██║██╔══██╗██╔══██║██╔══██║██║╚██╗██║
 ╚██████╔╝██║  ██║██║  ██║██║  ██║██║ ╚████║
  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝ 
```

# Proxy Wealth Detection System | Project UDAAN

Income lies. Spending patterns don't. This system identifies high-value customers where traditional financial signals fail.

## The Problem, Precisely

In many financial systems, income is the primary signal for creditworthiness. It is also misreported, unavailable, or inherently unreliable. 

**Observed Reality:**
* High-income individuals are not captured by standard metrics.
* Low-income proxies receive heavy misclassification.
* A large segment of "invisible high-value users" is entirely ignored.

**The Result:** Poor targeting, inefficient credit allocation, and missed high-LTV (Life Time Value) customers. The system does not fail due to a lack of data. It fails due to reliance on the wrong signals.

## The Solution

UDAAN reframes the core problem:
* **Not:** "Who earns more?"
* **But:** "Who behaves like a high-value customer?"

It builds a proxy-based prediction system that bypasses unreliable income data, leverages behavioral and transactional patterns, and translates statistical predictions into deployable field logic.

## System Architecture

```text
Raw Household Data (~50,000 records)
        │
        ▼
┌──────────────────────────────────┐
│ Feature Engineering              │
│ • Proxy Wealth Scoring           │
│ • Convenience Seeker Metrics     │
│ • Retailer Stocking Signals      │
└──────────────────────────────────┘
        │
        ▼
┌──────────────────────────────────┐
│ Gradient Boosting / Random Forest│
│ Output: Probability of           │
│ High-Value Customer              │
└──────────────────────────────────┘
        │
        ▼
┌──────────────────────────────────┐
│ Model Validation & Segmentation  │
│ • 5-fold Stratified CV           │
│ • AUC ≈ 0.92                     │
│ • K-Means (4 Behavioral Profiles)│
└──────────────────────────────────┘
        │
        ▼
┌──────────────────────────────────┐
│ Deployment Layer                 │
│ • Pilot District Scorecard       │
│ • Field-friendly indicators      │
│ • Zero reliance on income data   │
└──────────────────────────────────┘ 
```

## Core Metrics

| Metric | Value |
|--------|-------|
| **Dataset** | 50,000 households |
| **Models** | Gradient Boosting, Random Forest, K-Means |
| **Performance** | AUC 0.92 (GBM), AUC 0.90 (RF) |
| **Targeting** | Segmented 20K non-metro households into 4 profiles |
| **Outcome** | 150% improvement in targeting precision |

## Key Insights

### 1. Income is a weak signal
Reported income does not correlate strongly with actual spending behavior, leading to systematic misclassification. 

### 2. Behavioral proxies outperform financial inputs
Transaction patterns combined with consumption behavior yield significantly stronger predictive power than static demographic data.

### 3. Deployment is the real constraint
Models are useless if they cannot be executed in the field. Field agents cannot access back-end income data.
* **The Fix:** Replace hidden variables with observable proxies.
* **Example:** Instead of income, measure retail purchase behavior. Instead of declared assets, measure transaction frequency and basket size.

This transforms the model from a theoretical prediction into an execution-ready system.

## Business Impact

* Identified previously invisible high-value segments through K-Means clustering.
* Improved targeting efficiency by 150%.
* Eliminated dependency on unreliable income self-reporting.
* Enabled real-world deployment without requiring a massive infrastructure overhaul.

## Tech Stack

* **Languages & Libraries:** Python, Pandas, NumPy, Scikit-learn, Matplotlib
* **Modeling:** Gradient Boosting, Random Forest, K-Means Clustering
* **Validation:** 5-fold Stratified Cross-Validation

## Repository Structure

```text
udaan-proxy-wealth-detection/
│
├── notebooks/
│   └── UDAAN_Analysis.ipynb
├── data/
│   └── dataset.csv
├── outputs/
│   └── predictions.csv
└── README.md 
```

## Running the Project

**Via Google Colab (Recommended):**
1. File -> Open notebook -> GitHub
2. Paste the repository link.
3. Run all cells.

**Via Local Environment:**
```bash
git clone [https://github.com/tanx1509/udaan-proxy-wealth-detection](https://github.com/tanx1509/udaan-proxy-wealth-detection)
cd udaan-proxy-wealth-detection
pip install pandas numpy scikit-learn matplotlib jupyter
jupyter notebook notebooks/UDAAN_Analysis.ipynb 
```

---
*Built by Tanishq Sethi*
```
