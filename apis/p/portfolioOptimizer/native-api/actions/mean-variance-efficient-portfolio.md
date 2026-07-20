# Mean-Variance Efficient Portfolio with Portfolio Optimizer

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/portfolio/optimization/mean-variance-efficient`
- **Base URL:** `https://api.portfoliooptimizer.io`
- **Official documentation:** [Mean-Variance Efficient Portfolio](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/mean-variance-efficient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `G[]` | body | `array<array>` | no | Optional matrix defining asset groups. |
| `l[]` | body | `array<number>` | no | Optional minimum weights for each asset. |
| `mv_c` | body | `number` | no | Optional upper bound on portfolio volatility. |
| `r_c` | body | `number` | no | Optional target portfolio return. |
| `u_g[]` | body | `array<number>` | no | Optional maximum weights for the defined asset groups. |
| `u[]` | body | `array<number>` | no | Optional maximum weights for each asset. |
| `v_c` | body | `number` | no | Optional target portfolio volatility. |
| `w_max` | body | `number` | no | Optional upper bound on total portfolio exposure. |
| `w_min` | body | `number` | no | Optional lower bound on total portfolio exposure. |
