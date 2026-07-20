# <img src="https://images.mindcloud.co/apps/icons/88x88_1776273153668.png" alt="Portfolio Optimizer logo" width="28" height="28"> Portfolio Optimizer: Universal API

Portfolio Optimizer is a portfolio analytics and optimization API for returns, covariance, correlation, and allocation analysis.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/portfolioOptimizer/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://portfoliooptimizer.io/
- **Vendor API docs:** https://docs.portfoliooptimizer.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Asset Correlation Matrix](actions/asset-correlation-matrix.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/asset-correlation-matrix?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Asset Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Asset Mean Returns](actions/asset-mean-returns.md) | GET |  |
| [Asset Return Standard Deviation](actions/asset-return-standard-deviation.md) | GET |  |
| [Asset Return Variance](actions/asset-return-variance.md) | GET |  |
| [Asset Returns](actions/asset-returns.md) | GET |  |
| [Logarithmic Asset Returns](actions/logarithmic-asset-returns.md) | GET |  |

### Asset Matrix Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Asset Correlation Matrix](actions/asset-correlation-matrix.md) | GET |  |
| [Asset Covariance Matrix](actions/asset-covariance-matrix.md) | GET |  |
| [Distance Covariance Matrix](actions/distance-covariance-matrix.md) | GET |  |
| [Empirical Correlation Matrix](actions/empirical-correlation-matrix.md) | GET |  |
| [Empirical Covariance Matrix](actions/empirical-covariance-matrix.md) | GET |  |
| [EWMA Correlation Forecast](actions/ewma-correlation-forecast.md) | GET |  |
| [EWMA Covariance Forecast](actions/ewma-covariance-forecast.md) | GET |  |
| [Exponentially Weighted Correlation Matrix](actions/exponentially-weighted-correlation-matrix.md) | GET |  |
| [Exponentially Weighted Covariance Matrix](actions/exponentially-weighted-covariance-matrix.md) | GET |  |
| [Nearest Correlation Matrix](actions/nearest-correlation-matrix.md) | GET |  |
| [Perturbed Correlation Matrix](actions/perturbed-correlation-matrix.md) | GET |  |
| [Shrunk Correlation Matrix](actions/shrunk-correlation-matrix.md) | GET |  |
| [Shrunk Covariance Matrix](actions/shrunk-covariance-matrix.md) | GET |  |

### Portfolio Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Efficient Frontier](actions/efficient-frontier.md) | GET |  |
| [Portfolio Sharpe Ratio](actions/portfolio-sharpe-ratio.md) | GET |  |

### Portfolio Optimization

| Action | Method | Description |
| --- | --- | --- |
| [Diversified Mean-Variance Efficient Portfolio](actions/diversified-mean-variance-efficient-portfolio.md) | GET |  |
| [Equal Risk Contributions Portfolio](actions/equal-risk-contributions-portfolio.md) | GET |  |
| [Index Tracking Portfolio](actions/index-tracking-portfolio.md) | GET |  |
| [Maximum Return Portfolio](actions/maximum-return-portfolio.md) | GET |  |
| [Maximum Sharpe Ratio](actions/maximum-sharpe-ratio.md) | GET |  |
| [Mean-Variance Efficient Portfolio](actions/mean-variance-efficient-portfolio.md) | GET |  |
| [Minimum Correlation Portfolio](actions/minimum-correlation-portfolio.md) | GET |  |
| [Minimum Variance Portfolio](actions/minimum-variance-portfolio.md) | GET |  |
| [Most Diversified Portfolio](actions/most-diversified-portfolio.md) | GET |  |
| [Risk Budgeting Portfolio](actions/risk-budgeting-portfolio.md) | GET |  |

