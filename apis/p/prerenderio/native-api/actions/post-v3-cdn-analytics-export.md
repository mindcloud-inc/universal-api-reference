# Create Cdn Analytics Export with Prerender.io

Creates a CDN analytics export in Prerender.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/cdn-analytics-export`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Create Cdn Analytics Export](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `adaptive_type` | query | `string` | no |
| `cacheHit` | query | `string` | no |
| `fileType` | query | `string` | yes |
| `interval` | query | `string` | yes |
| `q` | query | `string` | no |
| `qCondition` | query | `string` | no |
| `renderedTimeHigh` | query | `number` | no |
| `renderedTimeLow` | query | `number` | no |
| `responseTimeHigh` | query | `number` | no |
| `responseTimeLow` | query | `number` | no |
| `sort` | query | `string` | no |
| `sortDirection` | query | `string` | no |
| `statusCodeEq` | query | `number` | no |
| `statusCodeHigh` | query | `number` | no |
| `statusCodeLow` | query | `number` | no |
| `timedout` | query | `boolean` | no |
| `userAgent` | query | `string` | no |
