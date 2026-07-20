# Create Billable Metric with Metronome

Creates a new billable metric in Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/billable-metrics/create`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Create Billable Metric](https://docs.metronome.com/api-reference/billable-metrics/create-a-billable-metric)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The billable metric name. |
| `aggregation_type` | body | `string` | yes | — |
| `event_type_filter.in_values[]` | body | `array<string>` | no | — |
