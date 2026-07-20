# Equal Risk Contributions Portfolio with Portfolio Optimizer

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/portfolio/optimization/equal-risk-contributions`
- **Base URL:** `https://api.portfoliooptimizer.io`
- **Official documentation:** [Equal Risk Contributions Portfolio](https://docs.portfoliooptimizer.io/index.html#post-/portfolio/optimization/equal-risk-contributions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `l[]` | body | `array<number>` | no | Optional minimum weights for each asset. |
| `u[]` | body | `array<number>` | no | Optional maximum weights for each asset. |
