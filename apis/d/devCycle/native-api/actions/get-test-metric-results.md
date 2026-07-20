# Get Test Metric Results with DevCycle

Retrieves test metric results from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/test-metric-results`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Test Metric Results](https://docs.devcycle.com/management-api/#tag/Metrics/operation/TestMetricResultsController_fetch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `control` | query | `string` | no | Control variation key. |
| `dimension` | query | `string` | no | Metric aggregation dimension. |
| `endDate` | query | `string` | no | Inclusive ISO-8601 end timestamp. |
| `event` | query | `string` | no | Metric event name. |
| `feature` | query | `string` | no | Feature key. |
| `optimize` | query | `string` | no | Optimization direction. |
| `project` | path | `string` | no | Project key. |
| `startDate` | query | `string` | no | Inclusive ISO-8601 start timestamp. |
