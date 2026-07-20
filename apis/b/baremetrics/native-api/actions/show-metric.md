# Show Metric with Baremetrics

Retrieves a metric from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/metrics/:metric`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Show Metric](https://developers.baremetrics.com/reference/show-metric)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metric` | path | `string` | yes | You can see a list of available metrics [here](available-metrics) |
| `start_date` | query | `string` | yes | — |
| `end_date` | query | `string` | yes | — |
| `compare_to` | query | `number` | no | The number of days ago to compare results to |
