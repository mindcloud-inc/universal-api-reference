# List Aggregated Metrics Usage Overview with Prerender.io

Retrieves a usage overview from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/aggregated-metrics/usage-overview`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Aggregated Metrics Usage Overview](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | — |
| `from` | query | `string` | yes | — |
| `timezoneOffset` | query | `number` | yes | Time zone offset in minutes |
