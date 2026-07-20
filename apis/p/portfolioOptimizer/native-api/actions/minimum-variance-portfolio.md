# Minimum Variance Portfolio with Portfolio Optimizer

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/portfolio/optimization/minimum-variance`
- **Base URL:** `https://api.portfoliooptimizer.io`
- **Official documentation:** [Minimum Variance Portfolio](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/minimum-variance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `G[]` | body | `array<array>` | no | Optional matrix defining asset groups. |
| `l[]` | body | `array<number>` | no | Optional minimum weights for each asset. |
| `mu[]` | body | `array<number>` | no | Optional returns vector to enforce mean-variance efficiency. |
| `u_g[]` | body | `array<number>` | no | Optional maximum weights for the defined asset groups. |
| `u[]` | body | `array<number>` | no | Optional maximum weights for each asset. |
| `w_max` | body | `number` | no | Optional upper bound on total portfolio exposure. |
| `w_min` | body | `number` | no | Optional lower bound on total portfolio exposure. |
