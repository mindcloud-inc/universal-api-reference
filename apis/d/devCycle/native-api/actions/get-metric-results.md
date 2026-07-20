# Get Metric Results with DevCycle

Retrieves results for a metric from DevCycle.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project/metrics/:key/results`
- **Base URL:** `https://api.devcycle.com`
- **Official documentation:** [Get Metric Results](https://docs.devcycle.com/management-api/#tag/Metrics/operation/MetricsController_fetchResults)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Inclusive ISO-8601 end timestamp. |
| `feature` | query | `string` | no | Feature key. |
| `key` | path | `string` | no | Metric key. |
| `project` | path | `string` | no | Project key. |
| `startDate` | query | `string` | no | Inclusive ISO-8601 start timestamp. |
