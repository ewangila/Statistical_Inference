# Statistical Inference Labs

Jupyter notebooks for classical statistical inference covering **means**, **proportions**, and **categorical data**. Each lab walks through research-question framing, exploratory analysis, assumption checks, hypothesis testing, effect-size interpretation, and practical recommendations.

---

## Labs Overview

| Notebook | Focus | Scenario | Key methods |
|----------|--------|----------|-------------|
| `stats_infer_mean_lab.ipynb` | Inference for means | Coral genotype growth for reef restoration | One-way ANOVA, Tukey’s HSD, η² |
| `stats_infer_proportion_lab.ipynb` | Inference for proportions | (Proportion-based research questions) | Proportion tests / confidence intervals |
| `stats_infer_cat_lab.ipynb` | Categorical data | Retail loyalty & promotional engagement | χ² tests of independence / goodness-of-fit |

---

## Business / Research Scenarios

### 1. Coral Genotype Growth (Means Lab)
A marine biology research center is evaluating six staghorn coral (*Acropora cervicornis*) genotypes grown in a nursery. The goal is to identify which genetic strains show superior linear growth and should be prioritized for reef restoration.

- **Data:** `data/coral_growth.csv` (Genotype, Growth_cm)
- **Primary test:** One-way ANOVA → Tukey’s HSD post-hoc
- **Effect size:** Eta-squared (η²)

### 2. Retail Promotional Engagement (Categorical Lab)
A retail chain wants to understand customer engagement with loyalty promotions (email, SMS, app notification), including whether engagement varies by time of day and whether certain channels drive higher purchase rates within 7 days.

- **Data:** `data/retail_promotions.csv`
- **Primary tests:** Chi-square tests of independence / related categorical procedures

---

### 3. Customer Retention at DataFlow (Proportions Lab)
You’ve joined DataFlow, a SaaS company that provides data visualization tools. The customer success team has been piloting a new onboarding program to improve 3-month retention. Your job is to estimate retention rates for both programs and test whether the new program delivers a statistically significant improvement.

- **Traditional onboarding:** 180 retained / 240 participants (75.0%)
- **New onboarding:** 210 retained / 260 participants (80.8%)
- **Primary methods:** 95% confidence intervals for each proportion + two-sample test for the difference in retention rates

## Project Structure

```text
Statistical_Inference/
├── data/
│   ├── coral_growth.csv
│   └── retail_promotions.csv
├── stats_infer_mean_lab.ipynb
├── stats_infer_proportion_lab.ipynb
├── stats_infer_cat_lab.ipynb
├── requirements.txt
├── LICENSE
├── .gitignore
└── README.md
```
## Setup & Usage

### Requirements

- Python 3.8+
- Jupyter Notebook or JupyterLab

### Install

```Bash
git clone https://github.com/ewangila/Statistical_Inference.git
cd Statistical_Inference
pip install -r requirements.txt
```
### Run the notebooks

```Bash
jupyter notebook
```
or
```Bash
jupyter lab
```
Open any of the three .ipynb files and run cells top-to-bottom.

Data files are loaded relative to the notebook (or from the data/ folder — adjust the path if needed).

### Dependencies

```text
pandas>=1.3.0
numpy>=1.20.0
scipy>=1.7.0
matplotlib>=3.4.0
seaborn>=0.11.0
statsmodels>=0.13.0
```
## Methods Snapshot (Means Lab)

1. **Hypothesis framing** – formal H₀ / H₁ for genotype differences  
2. **EDA** – summary statistics by genotype + boxplots  
3. **Assumption checks** – Shapiro–Wilk (normality), Levene’s test (homogeneity of variance)  
4. **One-way ANOVA** – overall test of mean differences  
5. **Post-hoc** – Tukey’s HSD for pairwise genotype comparisons  
6. **Effect size** – η² to quantify practical importance  
7. **Recommendations** – which genotypes to prioritize for restoration  

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

**Author:** Eugin Wangila  
**Location:** Nairobi
