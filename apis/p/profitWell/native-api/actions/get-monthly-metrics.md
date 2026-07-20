# Get Monthly Metrics with ProfitWell

Retrieves monthly metrics from ProfitWell.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/metrics/monthly`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Get Monthly Metrics](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `plan_id` | query | `string` | no | Optionally only return the metrics for this plan ID. |
| `metrics` | query | `string` | no | Optional comma-separated list of metrics trends to return. |
