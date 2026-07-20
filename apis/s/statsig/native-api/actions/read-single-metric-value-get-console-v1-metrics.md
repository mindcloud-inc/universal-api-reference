# Read Single Metric Value with Statsig

Retrieves a single metric value from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/metrics`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Read Single Metric Value](https://docs.statsig.com/api-reference/metrics/read-single-metric-value)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The unique identifier of the metric with format <metric_id>::<type> |
| `date` | query | `string` | yes | Expected valid date in the form of YYYY-MM-DD |
