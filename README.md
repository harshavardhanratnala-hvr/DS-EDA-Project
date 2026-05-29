[![Shipping files](https://github.com/neuefische/ds-eda-project-template/actions/workflows/workflow-03.yml/badge.svg?branch=main&event=workflow_dispatch)](https://github.com/neuefische/ds-eda-project-template/actions/workflows/workflow-03.yml)
# 📊 Case Study: King County Housing Market Anomaly Detection & Arbitrage

An academic-grade Exploratory Data Analysis (EDA) framework built on **21,500+ historical property records** to identify structural, geospatial, and seasonal pricing anomalies in King County, Washington. This project rejects traditional real estate guesswork, utilizing structured variable-interaction modeling ($Q \rightarrow Q$, $C \rightarrow Q$, and Multivariate analysis) to design a repeatable, data-backed capital deployment roadmap.


## Requirements

- pyenv
- python==3.11.3

## ⚙️ Setup

One of the first steps when starting any data science project is to create a virtual environment. For this project you have to create this environment from scratch yourself. However, you should be already familiar with the commands you will need to do so. The general workflow consists of... 

* setting the python version locally to 3.11.3
* creating a virtual environment using the `venv` module
* activating your newly created environment 
* upgrading `pip` (This step is not absolutely necessary, but will save you trouble when installing some packages.)
* installing the required packages via `pip`

*Note: We do have the `requirements.txt` in the repository but please try to first install packages by yourself.*

At the end, you want to make sure that people who are interested in your project can create an identical environment on their own computer in order to be able to run your code without running into errors. Therefore you can create a `requirements file` and add it to your repository. You can create such a file by running the following command: 

```bash
pip freeze > requirements.txt
```

*Note: In rare case such a requirements file created with `pip freeze` might not ensure that another (especially M1 chip) user can install and execute it properly. This can happen if libraries need to be compiled (e.g. SciPy). Then it also depends on environment variables and the actual system libraries.*


--- 
## In Case of Failure
If you fail to do the setup by yourself, then please revisit the previous repositories where you have done the setup and follow those steps.


# King County Housing Market: Predictive Feature Modeling & Real Estate Arbitrage


## 🎯 Project Overview & Objective
This analysis addresses a formalized business case aligned with an active investor/renovator stakeholder persona (**Charles Christensen**). The core objective is to maximize capital alpha by extracting systemic market pricing insights from non-linear distribution curves, geographical premiums, and temporal volume bottlenecks.

### ❓ Core Research Hypotheses:
1. **Temporal Vector ($Q \rightarrow Q$):** Real estate transaction volume and mean valuations follow distinct seasonal cyclicality, creating counter-cyclical winter buying opportunities and high-liquidity summer exit windows.
2. **Structural Vector ($C \rightarrow Q$):** Housing values scale exponentially rather than linearly across construction quality grade tiers, creating predictable arbitrage gaps.
3. **Geospatial Vector (Multivariate):** Specific high-demand zip codes maintain highly insulated price ceilings regardless of base building conditions, minimizing capital portfolio tail-risk.

---

## 🛠️ Tech Stack & Libraries Used
* **Language:** Python 3.11+
* **Environment:** Jupyter Notebook / Workspace
* **Core Analytics:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib` (including custom `patches` architectures), `seaborn`
* **Style Engine:** Custom high-contrast layout formatting optimized for both raw technical profiling and executive dark-mode presentations.

---

## 📈 Key Empirical Findings & Strategy

### 1. The "Winter Buy, Summer Fly" Framework ($Q \rightarrow Q$)
* **The Finding:** Mean housing valuations drop to a strict seasonal floor in **February at $508,520** while transaction volume hits its narrowest bottleneck. Conversely, prices spike to an average peak of **$562,216 in April** as spring volume surges by 146%.
* **Prescriptive Action:** Consistently acquire inventory during the winter bottleneck when competition is suppressed to secure an organic **10.5% value jump (~$53,000)** purely from market mechanics before starting construction.

### 2. The Exponential Value Grade Curve ($C \rightarrow Q$)
* **The Finding:** Value trends upward exponentially as properties cross structural thresholds. The mid-market residential baseline (**Grade 7**) maintains a dense distribution with a median of **$375,000**, whereas a **Grade 9 Custom Luxury** finish jumps the median value to **$720,000**.
* **Prescriptive Action:** Target highly available, low-entry Grade 7 frames and deploy capital to structurally re-engineer layouts, floorplans, and ceiling volumes to achieve a Grade 9 custom appraisal tier, unlocking a **+$345,000 value delta**.

### 3. High-Ceiling Geospatial Enclaves (Multivariate Spatial Analysis)
* **The Finding:** Custom structural value is heavily localized. Premier micro-markets like **98039 (Medina)** and **98004 (Bellevue)** display the county's highest willingness-to-pay for custom structural quality.
* **Prescriptive Action:** Target acquisitions along the geographical perimeters of these deep-capital zones (such as high-demand school districts) to capture an added **+14% exit velocity premium**, cutting expected asset holding durations in half.

### 4. Mathematical Validation (Pearson Correlation Coefficients)
* Continuous variables `sqft_living` ($r = 0.70$) and structural `grade` ($r = 0.67$) show absolute predictive authority over housing values. 
* Counter-intuitively, baseline home maintenance `condition` features a correlation score near zero ($r = 0.04$), proving that luxury buyers heavily favor foundational structural engineering and premium spatial footprints over simple cosmetic face-lifts.

---
## 📂 Repository Structure

```text
├── Data/
│   └── king_cunty_house_prices_dataset.csv   # Raw King County housing dataset (21,597 rows)
├── Output_Assets/
│   ├── correlation_matrix_dark.png           # Standalone high-res validation matrix
│   └── geospatial_premium_curved_dynamic.png # Custom patches-rendered presentation plot
├── .gitignore                                # Standard git exclusion configurations
├── EDA_Project.ipynb                         # Production-grade analytical Jupyter Notebook
├── README.md                                 # Comprehensive documentation and setup guide
├── requirements.txt                          # Operational environment package dependencies
└── Strategic_Investment_Roadmap.pdf          # Final stakeholder presentation deck (PDF)
```
---

## ⚙️ Data Preprocessing & Pipeline Execution

Once your virtual environment is activated and your requirements are installed via the main setup steps at the top of this page, you can initialize the pipeline:

1. Launch your Jupyter environment:
```bash
jupyter notebook EDA_Project.ipynb
```
2. Execute the notebook cells sequentially. Note: The script automatically handles data type serialization, including explicitly converting the zipcode variable into a string object to prevent type coercion during multi-feature correlation matrix calculations.