# List Aggregated Metrics Renders Daily with Prerender.io

Retrieves daily render metrics from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/aggregated-metrics/renders/daily`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Aggregated Metrics Renders Daily](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | — |
| `from` | query | `string` | yes | — |
| `timezoneOffset` | query | `number` | yes | Time zone offset in minutes |
