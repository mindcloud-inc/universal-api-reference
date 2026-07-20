# Reload metric data with Statsig

Reloads metric data in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/metrics/{id}/reload`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Reload metric data](https://docs.statsig.com/api-reference/metrics/reload-metric-data)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `incremental` | query | `string` | no | Incremental reload of the metric |
