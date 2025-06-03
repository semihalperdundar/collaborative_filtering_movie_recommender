<!--
═══════════════════════════════════════════════════════════════════════
README FOR “Collaborative Filtering Movie Recommender”
═══════════════════════════════════════════════════════════════════════
-->

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python">
  <img src="https://img.shields.io/badge/License-MIT-green">
  <img src="https://img.shields.io/badge/Build-Passing-brightgreen">
</p>

# 📽️ Collaborative Filtering Movie Recommender

An end-to-end recommender-system project that predicts movie ratings using **neighbourhood-based KNN** and **matrix-factorisation SVD** models (built with the [Surprise](https://surprise.readthedocs.io/) library).  
The workflow is demonstrated in **`CDA_complete_final.ipynb`** and achieves the following benchmark scores on a MovieLens-style dataset:

| Model                     | Sample Size | Best RMSE |
|---------------------------|-------------|-----------|
| Normal Predictor (baseline) | 100 %      | 1.4350 |
| KNNWithZScore             | 25 %        | 0.8410 |
| SVD                       | 81 %        | **0.7732** |

*(See the notebook for full hyper-parameter grids and cross-validation details.)*

---

## 📂 Table of Contents
1. [Project Motivation](#-project-motivation)
2. [Demo / Screenshots](#-demo--screenshots)
3. [Key Features](#-key-features)
4. [Project Structure](#-project-structure)
5. [Quick Start](#-quick-start)
6. [Usage](#-usage)
7. [Results & Evaluation](#-results--evaluation)
8. [Limitations & Future Work](#-limitations--future-work)
9. [Contributing](#-contributing)
10. [License](#-license)
11. [Acknowledgements](#-acknowledgements)

---

## 🚀 Project Motivation
Commercial platforms thrive on personalised recommendations, yet many public tutorials stop at toy examples.  
This repository shows how to:

* clean and **down-sample** large-scale rating data efficiently,
* explore sparsity patterns & temporal trends,
* tune 🔧 both **neighbourhood** and **latent-factor** models,
* compare models with cross-validated RMSE, and
* discuss reproducible pitfalls & next steps.

---

## 🎥 Demo / Screenshots
| Exploratory Analysis | Model Performance |
|----------------------|-------------------|
| ![EDA Histogram](docs/images/ratings_hist.png) | ![RMSE vs Epochs](docs/images/rmse_epochs.png) |

> All plots are generated directly from the notebook; run it end-to-end to reproduce them.

---

## ✨ Key Features
* **Pure-Python pipeline** (Pandas + Surprise + Matplotlib)  
* Configurable **train/validation/test** split & down-sampling percentage  
* Automatic grid search for KNN & SVD hyper-parameters  
* Handy utilities for **serialising** trained `AlgoBase` objects with `pickle`  
* Rich Markdown commentary explaining each decision step

---

## 🏗️ Project Structure
