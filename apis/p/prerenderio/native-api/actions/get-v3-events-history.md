# List Events History with Prerender.io

Retrieves event history from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/events-history`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Events History](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | query | `string` | no |
| `events` | query | `string` | no |
| `from` | query | `string` | yes |
| `page` | query | `number` | no |
| `pageSize` | query | `number` | no |
| `sort` | query | `string` | no |
| `sortDirection` | query | `string` | no |
| `to` | query | `string` | yes |
