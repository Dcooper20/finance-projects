# Quantitative Finance Projects

A collection of equity analysis and portfolio construction projects applying the Capital Asset Pricing Model (CAPM), the Fama–French factor model, and Modern Portfolio Theory to real market data.

Author: Delonta Cooper — [LinkedIn](https://www.linkedin.com/in/delontacooper/)

---

## 1. Equity Portfolio Optimization & Monte Carlo Simulation

Constructs and evaluates equity portfolios using factor-model-based expected returns, then maps the full risk–return space with a Monte Carlo simulation.

**What it does**
- Pulls monthly price data for a 10-stock universe and computes monthly returns.
- Estimates each stock's beta and equity risk premium using CAPM / the Fama–French factor model.
- Builds full covariance and correlation matrices across the assets to measure diversification.
- Runs a **Monte Carlo simulation of 10,000 randomly weighted portfolios**, computing the return series, expected excess return, standard deviation, and beta for each.
- Ranks every portfolio by risk-adjusted performance (**Sharpe ratio** and **Treynor ratio**) to identify the strongest allocations.

**Two versions are included:**
- *Diversified universe* — defensive names across utilities, consumer staples, and financials, priced against the **Fama–French 3-factor data** (market, size [SMB], and value [HML]). This version contains the 10,000-portfolio Monte Carlo simulation.
- *Technology universe* — large-cap tech (AAPL, MSFT, NVDA, and others), priced against **WRDS** data using a single-factor (market) CAPM approach.

**Techniques:** CAPM · Fama–French factor model · beta estimation · covariance & correlation analysis · Monte Carlo simulation · Sharpe & Treynor ratios

**Tools:** Excel · Python (pandas, NumPy)

**Data:** WRDS (Wharton Research Data Services) · Fama–French Data Library

**Files:**
- `Portfolio_Optimization_Diversified.xlsx` — diversified universe + 10,000-portfolio Monte Carlo simulation
- `Portfolio_Optimization_Tech.xlsx` — technology universe, constructed portfolios

---

## 2. CAPM Beta Estimation (Tableau)

An interactive Tableau workbook that estimates a stock's market beta — using Boeing as the example — and visualizes the CAPM relationship.

**What it does**
- Reconstructs market and stock excess returns (market return = market risk premium + risk-free rate; excess return = stock return − risk-free rate).
- Regresses the stock's excess returns against the market's excess returns to estimate **beta**.
- Compares results across two return frequencies (**daily vs. monthly**) and two regression specifications (**with a fitted intercept vs. forced through zero**) to test how stable the beta estimate is.
- Plots the **security characteristic line** and presents the specifications side by side.

**Techniques:** CAPM · beta estimation via linear regression · security characteristic line · excess-return analysis

**Tools:** Tableau · Excel

**Files:**
- `CAPM_Beta_Analysis.twbx` — packaged Tableau workbook

*Completed during my finance studies at DePaul University.*