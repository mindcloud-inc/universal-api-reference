# Retrieve Average Revenue Per Account (ARPA) with ChartMogul

Retrieves ARPA from ChartMogul.

## Endpoint

- **Method:** `GET`
- **Path:** `/metrics/arpa`
- **Base URL:** `https://api.chartmogul.com/v1`
- **Official documentation:** [Retrieve Average Revenue Per Account (ARPA)](https://dev.chartmogul.com/reference/metrics/arpa/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end-date` | query | `string` | yes | The end date for the metrics range in YYYY-MM-DD format. |
| `interval` | query | `string` | no | The reporting interval. Use values like day, week, month, quarter, or year. |
| `start-date` | query | `string` | yes | The start date for the metrics range in YYYY-MM-DD format. |
