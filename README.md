# Sovereign ESG Thresholds: Non-Linear Capital Flows & Machine Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

This repository contains the replication code, feature engineering pipeline, and machine learning architectures for the manuscript investigating the non-linear transmission mechanisms between sovereign Environmental, Social, and Governance (ESG) pillars and Foreign Direct Investment (FDI) inflows.

## Overview
Traditional macro-financial models frequently rely on linear econometric frameworks, inherently assuming that incremental improvements in sovereign ESG scores yield constant, proportional capital inflows. This study challenges that assumption. 

By deploying a Bayesian-optimised Extreme Gradient Boosting (XGBoost) architecture coupled with dual Explainable AI (SHAP and LIME) and Mondrian Split-Conformal Prediction, this pipeline mathematically maps the discrete, asymmetric thresholds ("tipping points") that dictate sovereign macro-financial resilience during systemic shocks.

## Repository Structure
The entire empirical pipeline—from SEC data extraction to high-dimensional econometrics—is housed within a single, sequential Jupyter Notebook to ensure seamless top-to-bottom reproducibility.

```text
├── data/
│   ├── Worldwide_Governance_Indicators_Extract/
|   │   ├── wgi_data.csv
├── Paper_1_notebook.ipynb          # MASTER NOTEBOOK
├── requirements.txt                # Python library dependencies
└── README.md
```


## Repository Contents
* `Paper-1.ipynb`: The primary Jupyter Notebook containing the full execution pipeline.
  * **Phase 1:** Forward-chaining panel data split and lag ($t-1$) engineering.
  * **Phase 2:** Baseline linear modelling (Lasso/SVR) and XGBoost Bayesian hyperparameter tournament.
  * **Phase 3:** Out-of-sample evaluation and modified Diebold-Mariano statistical testing.
  * **Phase 4:** Dual XAI consensus testing (SHAP/LIME) and threshold mapping.
  * **Phase 5:** Mondrian Conformal Prediction calibration and adversarial noise injection.
* `requirements.txt`: The exact Python library dependencies required to replicate the computational environment.


## Data Sources
To comply with journal data availability requirements, the raw macroeconomic and institutional data supporting this pipeline are fully public. The feature space merges data from:
1. **World Bank World Development Indicators (WDI)**
2. **Worldwide Governance Indicators (WGI)**

## Replication Instructions
To reproduce the methodology and generate the exact figures and loss-differentials cited in the manuscript:

1. Clone this repository:
```bash
   git clone [https://github.com/](https://github.com/)souravbose1991/sovereign-esg-thresholds.git
   cd sovereign-esg-thresholds
```
2. Install the required dependencies:
```bash
   pip install -r requirements.txt
```
3. Launch Jupyter and execute Paper_1_notebook.ipynb sequentially (after adjusting the filepaths).


## Citation
If you utilise this code or methodology in your own research, please cite the accompanying manuscript:

@article{bose2026beyond,
  title={Beyond Greenwashing: Algorithmic Resilience and the Non-Linear Governance Premium in Sovereign Capital Flows},
  author={Bose, Sourav and Bouraoui, Taoufik},
  journal={Working Paper, Rennes School of Business},
  year={2026}
}


## License
This project is licensed under the MIT License. See the LICENSE file for details.
