# Diversified Mean-Variance Efficient Portfolio with Portfolio Optimizer

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/portfolio/optimization/mean-variance-efficient/diversified`
- **Base URL:** `https://api.portfoliooptimizer.io`
- **Official documentation:** [Diversified Mean-Variance Efficient Portfolio](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/mean-variance-efficient/diversified)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `G[]` | body | `array<array>` | no | Optional matrix defining asset groups. |
| `l[]` | body | `array<number>` | no | Optional minimum weights for each asset. |
| `u_g[]` | body | `array<number>` | no | Optional maximum weights for the defined asset groups. |
| `u[]` | body | `array<number>` | no | Optional maximum weights for each asset. |
| `w_max` | body | `number` | no | Optional upper bound on total portfolio exposure. |
| `w_min` | body | `number` | no | Optional lower bound on total portfolio exposure. |
