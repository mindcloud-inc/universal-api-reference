# Retrieve Customer Churn Rate with ChartMogul

Retrieves customer churn rate from ChartMogul.

## Endpoint

- **Method:** `GET`
- **Path:** `/metrics/customer-churn-rate`
- **Base URL:** `https://api.chartmogul.com/v1`
- **Official documentation:** [Retrieve Customer Churn Rate](https://dev.chartmogul.com/reference/metrics/churn-rate/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end-date` | query | `string` | yes | The end date for the metrics range in YYYY-MM-DD format. |
| `interval` | query | `string` | no | The reporting interval. Use values like day, week, month, quarter, or year. |
| `start-date` | query | `string` | yes | The start date for the metrics range in YYYY-MM-DD format. |
