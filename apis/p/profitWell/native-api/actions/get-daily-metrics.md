# Get Daily Metrics with ProfitWell

Retrieves daily metrics from ProfitWell.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/metrics/daily`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Get Daily Metrics](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `month` | query | `string` | yes | Return daily metrics trends for this month in YYYY-MM format. Can only be the current or previous month. |
| `plan_id` | query | `string` | no | Optionally only return the metrics for this plan ID. |
| `metrics` | query | `string` | no | Optional comma-separated list of metrics trends to return. |
