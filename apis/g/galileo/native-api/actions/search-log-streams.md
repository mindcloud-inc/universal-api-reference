# Search Log Streams with Galileo

Finds log streams in a Galileo project by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects/:project_id/log_streams/search`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Search Log Streams](https://docs.galileo.ai/api-reference/log-stream/search-log-streams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
