## Results (Module 20.1)

### Research Question
Can daily log returns be treated as (approximately) stationary, and can simple models forecast short-horizon returns better than a naive baseline?

### Data
Daily Adjusted Close and Volume for [TICKERS] from [START_DATE] to [END_DATE]. Engineered features include log returns, lagged returns, rolling volatility (5/20-day), and volume change. Optional exogenous feature: SPY log return.

### Key EDA Findings
- Stock prices show strong trends (non-stationary), while log returns appear closer to stationary with mean near zero.
- Return distributions are heavy-tailed with occasional extreme outliers.
- Rolling volatility varies over time, with clear volatility clustering.

### Baseline Modeling
- Baseline 1 (Naive): predict 0 return for all days.
- Baseline 2 (Linear/Ridge): predict returns using lagged returns and engineered features.
- Evaluation used a time-based train/test split and RMSE/MSE on returns.

### Performance Summary
- Naive baseline RMSE: [X.XXXX]
- Linear/Ridge baseline RMSE: [X.XXXX]
- Directional accuracy (optional): [XX.X%]

### Takeaways / Business Interpretation
The data supports modeling returns (not raw prices). Predictive gains over a naive baseline are modest, suggesting limited short-term signal and a high risk of overfitting with complex models. Next steps include walk-forward validation, broader feature sets (market/volatility proxies), and careful comparison of ARMA vs regression-based approaches.
