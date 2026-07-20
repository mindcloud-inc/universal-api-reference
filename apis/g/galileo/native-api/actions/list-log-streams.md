# List Log Streams with Galileo

Finds log streams for a Galileo project.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/log_streams`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [List Log Streams](https://docs.galileo.ai/api-reference/log-stream/list-log-streams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
