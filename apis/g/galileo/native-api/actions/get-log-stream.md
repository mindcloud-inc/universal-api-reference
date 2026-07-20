# Get Log Stream with Galileo

Retrieves a log stream from Galileo by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/log_streams/:log_stream_id`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Log Stream](https://docs.galileo.ai/api-reference/log-stream/get-log-stream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `log_stream_id` | path | `string` | yes | Galileo log stream UUID. |
| `project_id` | path | `string` | yes | Galileo project UUID. |
