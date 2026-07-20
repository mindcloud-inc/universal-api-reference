# List Aggregated Metrics Page Delivered User Agent Daily with Prerender.io

Retrieves daily delivered page user agent metrics from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/aggregated-metrics/page-delivered-user-agent/daily`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Aggregated Metrics Page Delivered User Agent Daily](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | — |
| `from` | query | `string` | yes | — |
| `timezoneOffset` | query | `number` | yes | Time zone offset in minutes |
