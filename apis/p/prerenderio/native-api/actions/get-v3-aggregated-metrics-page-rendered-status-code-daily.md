# List Aggregated Metrics Page Rendered Status Code Daily with Prerender.io

Retrieves daily rendered page status code metrics from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/aggregated-metrics/page-rendered-status-code/daily`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Aggregated Metrics Page Rendered Status Code Daily](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | — |
| `from` | query | `string` | yes | — |
| `timezoneOffset` | query | `number` | yes | Time zone offset in minutes |
