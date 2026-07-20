# List Aggregated Metrics Status Codes with Prerender.io

Retrieves status code metrics from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/aggregated-metrics/status-codes`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Aggregated Metrics Status Codes](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawlers` | query | `list<string>` | yes | — |
| `dateFrom` | query | `string` | yes | — |
| `dateTo` | query | `string` | yes | — |
| `domain` | query | `string` | no | — |
| `firstDayOfWeek` | query | `number` | no | First day of the week (0 = Sunday, 1 = Monday, etc.) |
| `timezone` | query | `string` | no | — |
