# List Aggregated Metrics Cache Hits Ratio Summary with Prerender.io

Retrieves a cache hits ratio summary from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/aggregated-metrics/cache-hits-ratio-summary`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Aggregated Metrics Cache Hits Ratio Summary](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawlers` | query | `list<string>` | yes | — |
| `dateFrom` | query | `string` | yes | — |
| `dateTo` | query | `string` | yes | — |
| `domain` | query | `string` | no | — |
| `firstDayOfWeek` | query | `number` | no | First day of the week (0 = Sunday, 1 = Monday, etc.) |
| `timezone` | query | `string` | no | — |
