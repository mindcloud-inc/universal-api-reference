# Update Billable Metric with Metronome

Updates an existing billable metric in Metronome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/billable-metrics/:billable_metric_id`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Update Billable Metric](https://docs.metronome.com/api-reference/billable-metrics/update-a-billable-metric)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billable_metric_id` | path | `string` | yes | The billable metric ID. |
| `name` | body | `string` | yes | The new name of the metric. |
