# Get Metric with DevCycle

Retrieves a metric from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/metrics/:key`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Metric](https://docs.devcycle.com/management-api/#tag/Metrics/operation/MetricsController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | no | Metric key. |
| `project` | path | `string` | no | Project key. |
