# Read Metric Source Metrics with Statsig

Retrieves metric source metrics from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/metrics/metric_source/{name}/metrics`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Read Metric Source Metrics](https://docs.statsig.com/api-reference/metrics/read-metric-source-metrics)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
| `name` | path | `string` | yes | name |
