# Get Log Stream Metric Settings with Galileo

Retrieves metric settings for a Galileo log stream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/log_streams/:log_stream_id/metric_settings`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Log Stream Metric Settings](https://docs.galileo.ai/api-reference/log-stream/get-metric-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `log_stream_id` | path | `string` | yes | Galileo log stream UUID. |
| `project_id` | path | `string` | yes | Galileo project UUID. |
