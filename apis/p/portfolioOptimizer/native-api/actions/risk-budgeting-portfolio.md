# Risk Budgeting Portfolio with Portfolio Optimizer

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/portfolios/optimization/risk-budgeting`
- **Base URL:** `https://api.portfoliooptimizer.io`
- **Official documentation:** [Risk Budgeting Portfolio](https://docs.portfoliooptimizer.io/index.html#post-/portfolios/optimization/risk-budgeting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `l[]` | body | `array<number>` | no | Optional minimum weights for each asset. |
| `u[]` | body | `array<number>` | no | Optional maximum weights for each asset. |
