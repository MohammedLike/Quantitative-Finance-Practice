# 📘 Quantitative Finance Practice

This repository is a curated collection of **quantitative finance models and techniques** implemented in Python using Jupyter Notebooks. These notebooks were developed as part of my self-study and hands-on practice during the **Certificate in Quantitative Finance (CQF)** program. They cover key financial theories, pricing models, statistical techniques, and optimization methods, with a focus on practicality and intuition.

> 🚧 This is a learning-first repository – the code is not meant for production use but rather for understanding the underlying models.

---

## 🗂️ Table of Contents

- [📌 Asset Pricing & Financial Models](#-asset-pricing--financial-models)
- [📊 Quantitative Models & Techniques](#-quantitative-models--techniques)
- [🧮 Derivatives & Option Pricing](#-derivatives--option-pricing)
- [📈 Portfolio Theory & Optimization](#-portfolio-theory--optimization)
- [🧪 CQF-Specific Practice](#-cqf-specific-practice)
- [🎯 Purpose](#-purpose)
- [🧰 Tools Used](#-tools-used)
- [📌 Disclaimer](#-disclaimer)
- [👤 Author](#-author)
- [⭐️ Show Support](#️-show-support)

---

## 📌 Asset Pricing & Financial Models

### 🧩 `APT.ipynb`
- Implements **Arbitrage Pricing Theory (APT)** using multiple factor exposures.
- Shows how to decompose asset returns into sensitivities to macroeconomic or latent factors.
- **Key Concepts**: No-arbitrage condition, factor loading, linear pricing kernel.
- **Findings**: Linear regression can be used to estimate factor exposures and replicate CAPM when using market as a single factor.

### 🧮 `CAPM.ipynb`
- Applies the **Capital Asset Pricing Model (CAPM)** on real-world stock data.
- Estimates expected return from beta and calculates alpha for performance benchmarking.
- Visualizes the **Security Market Line (SML)** and explains over/underpriced assets.
- **Findings**: A stock’s position relative to the SML reveals if it's undervalued or overvalued.

### 📈 `Fama French.ipynb`
- Implements the **Fama-French 3-Factor Model** using regressions.
- Analyzes SMB (Size), HML (Value), and Market factors.
- **Finding**: Adds explanatory power over CAPM, especially for small-cap and value stocks.

### 🚀 `carhart.ipynb`
- Extends the Fama-French model with a **momentum factor** (UMD).
- Useful for evaluating mutual fund or hedge fund performance.
- **Finding**: Momentum persists and contributes to return predictability in certain markets.

---

## 📊 Quantitative Models & Techniques

### 🧠 `LinearRegression.ipynb`
- Demonstrates how to build and interpret a linear regression model.
- Applied to factor models, alpha/beta estimation, and residual diagnostics.
- **Techniques**: t-test, p-value, R², adjusted R², confidence intervals.
- **Finding**: Strong statistical significance does not always mean good predictive power.

### 📉 `vasicek model.ipynb`
- Implements the **Vasicek interest rate model** with mean reversion.
- Simulates short-rate dynamics and uses them to price zero-coupon bonds.
- **Applications**: Yield curve modeling, bond pricing, and interest rate derivatives.
- **Finding**: Interest rates don’t follow pure Brownian motion – they revert toward a long-term mean.

---

## 🧮 Derivatives & Option Pricing

### 📊 `One Period Binomial tree.ipynb`
- Classic **Cox-Ross-Rubinstein model** for a single step.
- Demonstrates replicating portfolios and risk-neutral valuation.
- **Finding**: Even simple discrete models yield intuitive understanding of hedging and payoff replication.

### 🌳 `modules1.ipynb`
- Extends to **multi-period binomial trees** for European and American options.
- Includes path-dependent valuation and tree visualization.
- **Use case**: Pricing American options or exotics like lookbacks and barriers.

---

## 📈 Portfolio Theory & Optimization

### 💼 `MPT.ipynb`
- Implements **Modern Portfolio Theory** by Harry Markowitz.
- Constructs efficient frontiers and identifies optimal risk-return portfolios.
- Calculates **Sharpe Ratio**, portfolio variance, and diversification benefits.
- **Finding**: Diversification works best when asset returns are uncorrelated.

### 🔧 `Optimization.ipynb`
- Uses `scipy.optimize` to build **custom portfolios** under constraints.
- Explores **objective functions** like minimizing volatility or maximizing Sharpe.
- **Extensions**: Add VaR, CVaR, or transaction cost constraints.

---

## 🧪 CQF Specific Practice

### 🧪 `CQF Practical.ipynb`
- A mix of practice problems aligned with CQF curriculum.
- Covers simulations, payoff visualizations, and closed-form solutions.
- **Finding**: Hands-on simulation helps internalize model behavior beyond formula memorization.

### 🛠️ `Notebook.ipynb`
- A sandbox notebook for ad-hoc experiments and code testing.
- Includes working snippets, trials of financial libraries, and drafts.

---

## 🎯 Purpose

This repository was created to:
- ✅ Reinforce theoretical finance concepts through practical coding
- ✅ Document learning progress throughout the CQF program
- ✅ Build a personal reference of working quant models
- ✅ Prepare for interviews and future quant research or trading roles

---

## 🧰 Tools Used

- **Language**: Python 3.x  
- **Environment**: Jupyter Notebooks  
- **Libraries**:  
  - `numpy`, `pandas`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`, `yfinance`

---

## 📌 Disclaimer

> This is a personal learning project. While accuracy is aimed for, models may be simplified, not fully validated, or optimized.  
> Always verify calculations before using for production, trading, or financial advice.



