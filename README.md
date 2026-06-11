# PCA Factor Models in Finance

---

# Overview

This repository contains our implementation of **Problem Statement 1** from the **QMP26 Case Study**:

> PCA Factor Models in Finance

The project explores the application of **Principal Component Analysis (PCA)** in quantitative finance for:

* latent factor discovery
* covariance structure analysis
* dimensionality reduction
* portfolio hedging
* reconstruction analysis
* rolling factor stability
* regime-shift robustness

The implementation combines statistical learning with portfolio construction techniques commonly used in quantitative trading and risk management.

---

# Problem Statement

We model synthetic stock prices using a latent factor process:

```math
P_{i,t} = P_{i,t-1} \cdot \exp(\mu_i + \beta_i f_t + \epsilon_{i,t})
```

where:

* (f_t) is a common market factor
* (\beta_i) represents factor loading
* (\epsilon_{i,t}) is idiosyncratic noise

Using PCA, we analyze the hidden factor structure governing asset returns.

---

# Repository Structure

```text
.
├── notebook/
│   └── Team_2.ipynb
│
├── src/
│   ├── generate_data.py
│   ├── covariance_analysis.py
│   ├── pca_analysis.py
│   ├── reconstruction.py
│   ├── portfolio.py
│   ├── rolling_pca.py
│   └── utils.py
│
└── plots
```

---

# Features

## Part 1 — Returns & Covariance Structure

* Synthetic stock-price generation
* Log-return computation
* Correlation & covariance heatmaps
* Return standardization

---

## Part 2 — PCA & Eigendecomposition

* Eigenvalue decomposition
* Scree plots
* Explained variance analysis
* Principal component interpretation
* PCA scores & loadings

---

## Part 3 — Reconstruction & Compression

* Dimensionality reduction
* Reconstruction using top-k PCs
* Reconstruction error analysis
* Covariance structure preservation

---

## Part 4 — Information Leakage

* Train-test PCA split
* Leakage quantification
* Out-of-sample explained variance
* Proper unsupervised evaluation

---

## Part 5 — Factor-Neutral Portfolios

* PC-neutral portfolio construction
* Portfolio backtesting
* Sharpe ratio analysis
* Maximum drawdown analysis
* Transaction-cost modeling

---

## Part 6 — Rolling PCA & Stability

* Rolling-window PCA
* Eigenvector drift analysis
* Sign-flip correction
* Regime-shift simulation
* Walk-forward backtesting

---

# Key Visualizations

## Correlation Heatmap

---

## Scree Plot

---

## Rolling PCA Stability

---

# Installation

Clone the repository:

```bash
git clone https://github.com/tiya27/PCA-Factor-Models-in-Finance
cd PCA-Factor-Models-in-Finance
```

Create virtual environment:

```bash
python -m venv venv
```

Activate environment:

### Windows

```bash
venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

---

# Requirements

Main libraries used:

* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy
* Jupyter

---

# Example Workflow

```python
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(returns)

pca = PCA()
pca.fit(X_scaled)

explained_variance = pca.explained_variance_ratio_
```

---

# Collaboration Workflow

This repository follows a branch-based collaboration workflow.

## Important Rules

* `main` branch is the stable production branch.
* Do NOT push experimental or unfinished code directly to `main`.
* Each team member must create and work on their own branch.

Example:

```bash
git checkout -b your-name-work
```

---

## Workflow

1. Pull latest changes from `main`
2. Work on your personal branch
3. Commit changes regularly
4. Push your branch to GitHub
5. Open a Pull Request before merging into `main`

---

## Example Commands

### Create your branch

```bash
git checkout -b your-name-work
```

### Push your branch

```bash
git push -u origin your-name-work
```

### Pull latest main updates

```bash
git checkout main
git pull origin main
```

---

## Important

Do not overwrite or directly edit another member's branch without coordination.

The `main` branch should always remain clean, runnable, and presentation-ready.


# Financial Insights

Key observations from the project include:

* PC1 typically captures the market-wide movement factor
* PCA compression preserves most covariance information with few components
* Information leakage inflates out-of-sample explained variance
* Rolling PCA reveals instability during regime changes
* Factor-neutral portfolios reduce systematic exposure but increase turnover costs

---

# Technologies Used

| Category             | Tools               |
| -------------------- | ------------------- |
| Programming          | Python              |
| Data Analysis        | NumPy, Pandas       |
| Visualization        | Matplotlib, Seaborn |
| Machine Learning     | Scikit-learn        |
| Scientific Computing | SciPy               |
| Development          | Jupyter Notebook    |

---

# Team Members

* Tiya
* Tejasvini
* Yogita

---

# Future Improvements

#
