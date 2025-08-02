# Quantitative Finance Practice Repository

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![CQF](https://img.shields.io/badge/CQF-Certificate%20Program-red.svg)](https://www.cqf.com/)

A comprehensive collection of quantitative finance models and techniques implemented in Python, developed during my Certificate in Quantitative Finance (CQF) journey. This repository bridges the gap between financial theory and practical implementation, offering rigorous implementations of key financial models.

## Table of Contents

- [Overview](#overview)
- [Quick Start](#quick-start)
- [Repository Structure](#repository-structure)
- [Asset Pricing Models](#asset-pricing-models)
- [Derivatives Pricing](#derivatives-pricing)
- [Portfolio Optimization](#portfolio-optimization)
- [Quantitative Methods](#quantitative-methods)
- [CQF Practice](#cqf-practice)
- [Technical Requirements](#technical-requirements)
- [Installation](#installation)

## Overview

This repository contains implementations of fundamental quantitative finance models, developed as part of my CQF studies. Each notebook provides:

- **Theoretical Foundation**: Mathematical derivations and economic intuition
- **Implementation**: Clean, well-documented Python code
- **Validation**: Statistical tests and model diagnostics
- **Applications**: Real-world use cases and interpretations

The code is designed for educational purposes and understanding of underlying models rather than production deployment.

## Quick Start

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Installation
```bash
git clone https://github.com/MohammedLike/quantitative-finance-practice.git
cd quantitative-finance-practice
pip install -r requirements.txt
jupyter notebook
```

### Core Dependencies
```
numpy>=1.21.0
pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0
scipy>=1.7.0
statsmodels>=0.12.0
yfinance>=0.1.70
scikit-learn>=1.0.0
```

## Repository Structure

```
quantitative-finance-practice/
├── APT.ipynb                    # Arbitrage Pricing Theory
├── CAPM.ipynb                   # Capital Asset Pricing Model
├── Fama French.ipynb            # Fama-French Three-Factor Model
├── carhart.ipynb                # Carhart Four-Factor Model
├── One Period Binomial tree.ipynb  # Single-Period Binomial Model
├── modules1.ipynb               # Multi-Period Binomial Trees
├── MPT.ipynb                    # Modern Portfolio Theory
├── Optimization.ipynb           # Portfolio Optimization
├── LinearRegression.ipynb       # Linear Regression in Finance
├── vasicek model.ipynb          # Vasicek Interest Rate Model
├── CQF Practical.ipynb          # CQF Practice Problems
├── Notebook.ipynb               # Research Sandbox
├── requirements.txt
└── README.md
```

## Asset Pricing Models

### Arbitrage Pricing Theory (APT)
**File**: `APT.ipynb`

Implementation of Ross's APT framework for multi-factor asset pricing.

**Key Features**:
- Multiple factor model construction using principal component analysis
- Factor loading estimation through cross-sectional regression
- No-arbitrage condition testing and verification
- Comparison with CAPM as a single-factor special case

**Mathematical Framework**:
```
E[R_i] = λ_0 + β_i1λ_1 + β_i2λ_2 + ... + β_ikλ_k
```

**Applications**:
- Cross-sectional return prediction
- Factor-based investment strategies
- Portfolio risk attribution analysis

### Capital Asset Pricing Model (CAPM)
**File**: `CAPM.ipynb`

Classic Sharpe-Lintner CAPM implementation with empirical testing.

**Components**:
- Beta estimation using rolling window regression
- Alpha calculation for performance evaluation
- Security Market Line construction and visualization
- Statistical significance testing of alpha and beta

**Core Equation**:
```
E[R_i] = R_f + β_i(E[R_m] - R_f)
```

**Analysis Includes**:
- Time-varying beta estimation
- Market efficiency tests
- Asset mispricing identification

### Fama-French Three-Factor Model
**File**: `Fama French.ipynb`

Extension of CAPM incorporating size and value factors.

**Factor Construction**:
- **Market Factor (Rm-Rf)**: Excess market return
- **Size Factor (SMB)**: Small minus big market capitalization effect
- **Value Factor (HML)**: High minus low book-to-market ratio effect

**Enhanced Explanatory Power**:
- Significant improvement in R-squared over CAPM
- Better explanation of cross-sectional return variations
- Foundation for factor-based portfolio construction

### Carhart Four-Factor Model
**File**: `carhart.ipynb`

Four-factor model incorporating momentum alongside Fama-French factors.

**Additional Factor**:
- **Momentum (UMD)**: Up minus down (winner minus loser stocks)

**Applications**:
- Mutual fund performance evaluation
- Risk-adjusted return measurement
- Momentum strategy analysis

## Derivatives Pricing

### Binomial Option Pricing Model
**Files**: `One Period Binomial tree.ipynb`, `modules1.ipynb`

Cox-Ross-Rubinstein binomial model implementation from single to multi-period.

**Single Period Model**:
- Risk-neutral valuation principles
- Replicating portfolio construction
- Delta hedging demonstration

**Multi-Period Extension**:
- Backward induction pricing methodology
- American option early exercise analysis
- Path-dependent option pricing

**Model Parameters**:
```
u = exp(σ√Δt)               # Up movement factor
d = 1/u                     # Down movement factor
q = (e^(rΔt) - d)/(u - d)   # Risk-neutral probability
```

## Portfolio Optimization

### Modern Portfolio Theory (MPT)
**File**: `MPT.ipynb`

Markowitz mean-variance optimization framework implementation.

**Core Components**:
- Efficient frontier construction through quadratic programming
- Risk-return trade-off analysis
- Optimal portfolio weight calculation
- Diversification benefit quantification

**Optimization Problem**:
```
minimize: w^T Σ w
subject to: w^T μ = μ_target
           w^T 1 = 1
```

**Key Insights**:
- Correlation impact on diversification
- Risk-free asset integration
- Capital allocation line construction

### Advanced Portfolio Optimization
**File**: `Optimization.ipynb`

Extended optimization techniques beyond standard MPT.

**Alternative Objectives**:
- Sharpe ratio maximization
- Risk parity portfolio construction
- Minimum variance portfolio optimization
- Maximum diversification ratio

**Constraint Handling**:
- Long-only constraints
- Position size limits  
- Sector allocation constraints
- Transaction cost incorporation

## Quantitative Methods

### Linear Regression Applications
**File**: `LinearRegression.ipynb`

Statistical foundations for financial modeling using ordinary least squares.

**Topics Covered**:
- OLS assumptions and diagnostic testing
- Heteroscedasticity detection and correction
- Autocorrelation analysis using Durbin-Watson test
- Multicollinearity assessment via variance inflation factors

**Financial Applications**:
- Beta estimation for CAPM
- Factor model construction
- Performance attribution analysis
- Risk model development

### Interest Rate Modeling
**File**: `vasicek model.ipynb`

Vasicek short-rate model for term structure analysis.

**Model Specification**:
```
dr(t) = κ(θ - r(t))dt + σ dW(t)
```

**Key Properties**:
- Mean reversion to long-term rate θ
- Gaussian interest rate distribution
- Closed-form solutions for bond prices
- Analytical formula for option pricing

**Implementation Features**:
- Parameter estimation via maximum likelihood
- Monte Carlo simulation of rate paths
- Zero-coupon bond pricing
- Model calibration to market data

## CQF Practice

### Integrated CQF Problems
**File**: `CQF Practical.ipynb`

Comprehensive problems spanning multiple CQF modules.

**Module Coverage**:
- Building blocks of quantitative finance
- Quantitative risk and return analysis
- Equity and currency modeling
- Fixed income and credit analysis
- Advanced derivatives pricing

### Research and Development
**File**: `Notebook.ipynb`

Experimental workspace for testing new concepts and methodologies.

**Research Areas**:
- Model extensions and improvements
- Alternative data integration
- Machine learning applications in finance
- Custom indicator development

## Technical Requirements

### System Specifications
- **Operating System**: Windows 10+, macOS 10.14+, Ubuntu 18.04+
- **Python Version**: 3.8 or higher
- **Memory**: 8GB RAM recommended for large dataset operations
- **Storage**: 2GB free space for data and dependencies

### Performance Considerations
- Vectorized computations using NumPy for efficiency
- Optimized data structures with Pandas
- Parallel processing capabilities for simulation-intensive models
- Memory-efficient handling of financial time series data

## Installation

### Step-by-Step Setup

1. **Clone Repository**
   ```bash
   git clone https://github.com/MohammedLike/quantitative-finance-practice.git
   cd quantitative-finance-practice
   ```

2. **Create Virtual Environment** (Recommended)
   ```bash
   python -m venv qf_env
   source qf_env/bin/activate  # On Windows: qf_env\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter**
   ```bash
   jupyter notebook
   ```

**Disclaimer**: This repository is intended for educational and research purposes. While every effort has been made to ensure accuracy, the implementations should be thoroughly validated before any practical application. The author assumes no responsibility for any financial decisions made based on this code.

