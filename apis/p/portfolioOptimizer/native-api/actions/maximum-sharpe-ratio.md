# Maximum Sharpe Ratio with Portfolio Optimizer

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/portfolio/optimization/maximum-sharpe-ratio`
- **Base URL:** `https://api.portfoliooptimizer.io`
- **Official documentation:** [Maximum Sharpe Ratio](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/maximum-sharpe-ratio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `G[]` | body | `array<array>` | no | Optional matrix defining asset groups. |
| `l[]` | body | `array<number>` | no | Optional minimum weights for each asset. |
| `mu[]` | body | `array<number>` | yes | Required asset arithmetic returns vector. |
| `r_f` | body | `number` | yes | Required risk-free rate. |
| `Sigma[]` | body | `array<array>` | yes | Required asset covariance matrix. |
| `u_g[]` | body | `array<number>` | no | Optional maximum weights for the defined asset groups. |
| `u[]` | body | `array<number>` | no | Optional maximum weights for each asset. |
| `w_max` | body | `number` | no | Optional upper bound on total portfolio exposure. |
| `w_min` | body | `number` | no | Optional lower bound on total portfolio exposure. |
