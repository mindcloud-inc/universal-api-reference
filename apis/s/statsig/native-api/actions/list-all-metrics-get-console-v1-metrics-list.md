# List all Metrics with Statsig

Retrieves all metrics from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/metrics/list`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List all Metrics](https://docs.statsig.com/api-reference/metrics/list-all-metrics)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `showHiddenMetrics` | query | `string` | no | Should hidden metrics be returned: Allowed values are "true" or "false". |
| `tags` | query | `string` | no | Filter metrics based on a given tagID, found on /tags endpoint. Can be a single string or an array of strings. |
| `filters` | query | `string` | no | Additional filters for metrics. Can be a string or an object with tags filter. |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
