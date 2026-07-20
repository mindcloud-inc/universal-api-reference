# List Aggregated Metrics Page Delivered User Agent Overview with Prerender.io

Retrieves an overview of delivered page user agent metrics from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/aggregated-metrics/page-delivered-user-agent/overview`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Aggregated Metrics Page Delivered User Agent Overview](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | — |
| `from` | query | `string` | yes | — |
| `timezoneOffset` | query | `number` | yes | Time zone offset in minutes |
