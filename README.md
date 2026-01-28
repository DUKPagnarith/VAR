# Portfolio Risk Measurement Using Value-at-Risk and Conditional Value-at-Risk

A comprehensive financial risk analysis project that measures portfolio risk using advanced quantitative methods on stocks from the Stock Exchange of Cambodia.

**[View Live Report](https://dukpagnarith.github.io/VAR/)**

## Overview

This project demonstrates modern portfolio risk management techniques by:

- Constructing an **efficient frontier** using mean-variance optimization on 9 Cambodian stocks
- Selecting a balanced portfolio from the efficient frontier
- Measuring risk using **Value-at-Risk (VaR)** and **Conditional Value-at-Risk (CVaR)**
- Comparing three methodological approaches for risk estimation
- Validating VaR models through **Kupiec backtesting**
- Analyzing tail risk and the role of asset correlations

## Key Insight

Traditional variance-based risk measures treat gains and losses symmetrically, but investors primarily care about **downside risk**. VaR and CVaR provide loss-focused measures that better reflect investor concerns.

## Methodologies

The project compares three VaR/CVaR estimation methods:

| Method | Description | Pros | Cons |
|--------|-------------|------|------|
| **Parametric** | Assumes normal distribution | Fast, analytically tractable | May underestimate tail risk |
| **Historical Simulation** | Uses empirical quantiles | No distributional assumptions | Limited by historical data |
| **Monte Carlo** | 100,000 simulated scenarios | Captures correlations explicitly | Computationally intensive |

## Data

The analysis uses daily log returns from 9 stocks listed on the Stock Exchange of Cambodia:

- **PWSA** - Phnom Penh Water Supply Authority
- **ABC** - ACLEDA Bank Plc
- **GTI** - Grand Twins International
- **PAS** - Sihanoukville Autonomous Port
- **PEPC** - PESTECH
- **PPAP** - Phnom Penh Autonomous Port
- **PPSP** - Phnom Penh Special Economic Zone Plc
- **CGSM** - CAMGSM Plc (Cellcard)
- **MJQE** - Mengly J. Quach Education Plc

## Project Structure

```
Financial_Value_at_risk/
├── index.qmd              # Main Quarto notebook with analysis
├── index.html             # Rendered HTML report
├── Log_return.csv         # Stock returns data
├── Value_at_risk_files/   # Generated figures and assets
└── README.md
```

## Technologies

- **Python 3** - Core analysis
- **Quarto** - Document generation
- **NumPy** - Numerical computations
- **Pandas** - Data manipulation
- **SciPy** - Statistical functions and optimization
- **Matplotlib** - Visualizations

## Analysis Sections

1. **Introduction** - Risk concepts and methodology overview
2. **Data Collection** - Loading and exploring stock returns
3. **Efficient Frontier** - Constructing optimal portfolios
4. **Portfolio Selection** - Choosing a balanced portfolio
5. **Portfolio Returns** - Computing daily portfolio returns
6. **Parametric VaR/CVaR** - Normal distribution approach
7. **Historical Simulation** - Empirical quantile approach
8. **Monte Carlo VaR/CVaR** - Simulation-based approach
9. **Method Comparison** - Comparing all three approaches
10. **Sensitivity Analysis** - VaR across confidence levels
11. **Kupiec Backtesting** - Model validation
12. **Conclusions** - Summary and recommendations

## Key Visualizations

- Efficient frontier with individual assets
- Portfolio composition breakdown
- Returns distribution with VaR/CVaR thresholds
- Method comparison charts
- Backtesting violation timeseries
- Q-Q plots for normality diagnostics

## Regulatory Framework

The project references:
- **Basel III** capital requirements framework
- **Basel traffic light system** (Green/Yellow/Red zones)
- **Kupiec POF test** for backtesting validation

## Running the Analysis

1. Ensure Python 3 and required libraries are installed:
   ```bash
   pip install numpy pandas scipy matplotlib
   ```

2. Install Quarto from [quarto.org](https://quarto.org/)

3. Render the report:
   ```bash
   quarto render index.qmd
   ```

## License

This project is for educational purposes in financial risk management.

## Author

Duk Pagnarith

---

*This analysis demonstrates quantitative portfolio risk management techniques suitable for finance students, risk managers, and portfolio analysts learning VaR methodologies.*
