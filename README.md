# Nifty 50 — Equity Volatility Regime Detection & Forecasting

**AFTS Project | M.Sc. Data Science | NMIMS**

---

## Research Question
> Do asymmetric GARCH models outperform standard GARCH in forecasting Nifty 50 volatility across different market regimes, and how does this affect Value-at-Risk estimation?

---

## Project Structure

```
nifty50-volatility-regime-forecasting/
│
├── 01_data_collection_eda.ipynb          # Data download, cleaning, EDA, stationarity tests
├── 02_classical_models.ipynb             # ARIMA, STL decomposition, Exponential Smoothing
├── 03_garch_volatility_models.ipynb      # ARCH, GARCH, EGARCH, GJR-GARCH, HMM regimes
├── 04_var_backtesting.ipynb              # VaR, Expected Shortfall, Kupiec, Diebold-Mariano
├── 05_hybrid_pipeline_final.ipynb        # ARIMA-GARCH hybrid, dashboard, conclusions
│
├── data/                                 # Generated data files (created at runtime)
│   ├── nifty50_master.csv
│   ├── arima_residuals.csv
│   ├── arima_best_order.csv
│   ├── hmm_regimes.csv
│   └── ...
│
├── plots/                                # All generated figures
│
├── requirements.txt
└── README.md
```

---

## Techniques Covered

| Technique | Notebook | Purpose |
|---|---|---|
| Log-return computation | 01 | Stationarity, % returns |
| ADF & KPSS tests | 01 | Unit root / stationarity |
| ACF / PACF analysis | 01, 02 | AR/MA order identification |
| Jarque-Bera test | 01 | Non-normality of returns |
| ARIMA(p,0,q) | 02 | Conditional mean forecast |
| STL Decomposition | 02 | Trend + seasonality extraction |
| Holt-Winters | 02 | Exponential smoothing baseline |
| Engle ARCH LM test | 03 | Confirm heteroscedasticity |
| ARCH(q) | 03 | Baseline conditional variance |
| GARCH(1,1) | 03 | Standard volatility model |
| EGARCH(1,1) | 03 | Leverage effect (asymmetry) |
| GJR-GARCH(1,1,1) | 03 | Alternative asymmetric model |
| News Impact Curve | 03 | Visualise asymmetric response |
| HMM (3-state) | 03 | Regime detection |
| Value at Risk (VaR) | 04 | 99%/95% downside risk |
| Expected Shortfall (ES) | 04 | Tail risk beyond VaR |
| Kupiec POF Test | 04 | VaR backtest |
| Christoffersen Test | 04 | Independence of violations |
| Diebold-Mariano Test | 04 | Statistical forecast comparison |
| ARIMA-GARCH Hybrid | 05 | Joint mean + variance model |
| Regime-conditional VaR | 05 | Risk by market state |

---

## Setup

```bash
pip install -r requirements.txt
```

Run notebooks in order: 01 → 02 → 03 → 04 → 05

---

## Requirements
See `requirements.txt`
