# List Log Streams Paginated with Galileo

Finds log streams for a Galileo project with pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/log_streams/paginated`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [List Log Streams Paginated](https://docs.galileo.ai/api-reference/log-stream/list-log-streams-paginated)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
