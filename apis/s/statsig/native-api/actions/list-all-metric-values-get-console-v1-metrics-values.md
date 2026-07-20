# List All Metric Values with Statsig

Retrieves all metric values from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/metrics/values`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List All Metric Values](https://docs.statsig.com/api-reference/metrics/list-all-metric-values)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Expected valid date in the form of YYYY-MM-DD |
| `metricName` | query | `string` | no | — |
| `metricType` | query | `string` | no | — |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
