# Retrieve All Key Metrics with ChartMogul

Retrieves all key metrics from ChartMogul.

## Endpoint

- **Method:** `GET`
- **Path:** `/metrics/all`
- **Base URL:** `https://api.chartmogul.com/v1`
- **Official documentation:** [Retrieve All Key Metrics](https://dev.chartmogul.com/reference/metrics/all/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end-date` | query | `string` | yes | The end date for the metrics range in YYYY-MM-DD format. |
| `interval` | query | `string` | no | The reporting interval. Use values like day, week, month, quarter, or year. |
| `start-date` | query | `string` | yes | The start date for the metrics range in YYYY-MM-DD format. |
