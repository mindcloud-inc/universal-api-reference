# Portfolio Optimizer: Native API Reference

A consolidated summary of Portfolio Optimizer's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.portfoliooptimizer.io/
- **API base URL:** `https://api.portfoliooptimizer.io`

## Authentication

### No Authentication

This API does not require request authentication.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Asset Correlation Matrix](actions/asset-correlation-matrix.md) | `POST /v1/assets/correlation/matrix` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/correlation/matrix) |
| [Asset Covariance Matrix](actions/asset-covariance-matrix.md) | `POST /v1/assets/covariance/matrix` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/covariance/matrix) |
| [Asset Mean Returns](actions/asset-mean-returns.md) | `POST /v1/assets/returns/mean` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/returns/mean) |
| [Asset Return Standard Deviation](actions/asset-return-standard-deviation.md) | `POST /v1/assets/returns/standard-deviation` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/returns/standard-deviation) |
| [Asset Return Variance](actions/asset-return-variance.md) | `POST /v1/assets/returns/variance` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/returns/variance) |
| [Asset Returns](actions/asset-returns.md) | `POST /v1/assets/returns` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/returns) |
| [Distance Covariance Matrix](actions/distance-covariance-matrix.md) | `POST /v1/assets/covariance/matrix/estimation/distance` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/covariance/matrix/estimation/distance) |
| [Diversified Mean-Variance Efficient Portfolio](actions/diversified-mean-variance-efficient-portfolio.md) | `POST /v1/portfolio/optimization/mean-variance-efficient/diversified` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/mean-variance-efficient/diversified) |
| [Efficient Frontier](actions/efficient-frontier.md) | `POST /v1/portfolios/analysis/mean-variance/efficient-frontier` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolios/analysis/mean-variance/efficient-frontier) |
| [Empirical Correlation Matrix](actions/empirical-correlation-matrix.md) | `POST /v1/assets/correlation/matrix/estimation/empirical` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/correlation/matrix/estimation/empirical) |
| [Empirical Covariance Matrix](actions/empirical-covariance-matrix.md) | `POST /v1/assets/covariance/matrix/estimation/empirical` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/covariance/matrix/estimation/empirical) |
| [Equal Risk Contributions Portfolio](actions/equal-risk-contributions-portfolio.md) | `POST /v1/portfolio/optimization/equal-risk-contributions` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/equal-risk-contributions) |
| [EWMA Correlation Forecast](actions/ewma-correlation-forecast.md) | `POST /v1/assets/correlation/matrix/forecast/ewma` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/correlation/matrix/forecast/ewma) |
| [EWMA Covariance Forecast](actions/ewma-covariance-forecast.md) | `POST /v1/assets/covariance/matrix/forecast/ewma` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/covariance/matrix/forecast/ewma) |
| [Exponentially Weighted Correlation Matrix](actions/exponentially-weighted-correlation-matrix.md) | `POST /v1/assets/correlation/matrix/estimation/empirical/exponentially-weighted` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/correlation/matrix/estimation/empirical/exponentially-weighted) |
| [Exponentially Weighted Covariance Matrix](actions/exponentially-weighted-covariance-matrix.md) | `POST /v1/assets/covariance/matrix/estimation/empirical/exponentially-weighted` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/covariance/matrix/estimation/empirical/exponentially-weighted) |
| [Index Tracking Portfolio](actions/index-tracking-portfolio.md) | `POST /v1/portfolios/replication/index-tracking` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolios/replication/index-tracking) |
| [Logarithmic Asset Returns](actions/logarithmic-asset-returns.md) | `POST /v1/assets/returns/logarithmic` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/returns/logarithmic) |
| [Maximum Return Portfolio](actions/maximum-return-portfolio.md) | `POST /v1/portfolio/optimization/maximum-return` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/maximum-return) |
| [Maximum Sharpe Ratio](actions/maximum-sharpe-ratio.md) | `POST /v1/portfolio/optimization/maximum-sharpe-ratio` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/maximum-sharpe-ratio) |
| [Mean-Variance Efficient Portfolio](actions/mean-variance-efficient-portfolio.md) | `POST /v1/portfolio/optimization/mean-variance-efficient` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/mean-variance-efficient) |
| [Minimum Correlation Portfolio](actions/minimum-correlation-portfolio.md) | `POST /v1/portfolio/optimization/minimum-correlation` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/minimum-correlation) |
| [Minimum Variance Portfolio](actions/minimum-variance-portfolio.md) | `POST /v1/portfolio/optimization/minimum-variance` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/minimum-variance) |
| [Most Diversified Portfolio](actions/most-diversified-portfolio.md) | `POST /v1/portfolio/optimization/most-diversified` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/most-diversified) |
| [Nearest Correlation Matrix](actions/nearest-correlation-matrix.md) | `POST /v1/assets/correlation/matrix/nearest` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/correlation/matrix/nearest) |
| [Perturbed Correlation Matrix](actions/perturbed-correlation-matrix.md) | `POST /v1/assets/correlation/matrix/perturbed` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/correlation/matrix/perturbed) |
| [Portfolio Sharpe Ratio](actions/portfolio-sharpe-ratio.md) | `POST /v1/portfolios/analysis/mean-variance/sharpe-ratio` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolios/analysis/mean-variance/sharpe-ratio) |
| [Risk Budgeting Portfolio](actions/risk-budgeting-portfolio.md) | `POST /v1/portfolios/optimization/risk-budgeting` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/portfolios/optimization/risk-budgeting) |
| [Shrunk Correlation Matrix](actions/shrunk-correlation-matrix.md) | `POST /v1/assets/correlation/matrix/estimation/empirical/shrunk` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/correlation/matrix/estimation/empirical/shrunk) |
| [Shrunk Covariance Matrix](actions/shrunk-covariance-matrix.md) | `POST /v1/assets/covariance/matrix/estimation/empirical/shrunk` | [docs](https://docs.portfoliooptimizer.io/index.html#post-/assets/covariance/matrix/estimation/empirical/shrunk) |
