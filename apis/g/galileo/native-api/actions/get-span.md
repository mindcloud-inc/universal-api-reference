# Get Span with Galileo

Retrieves a span from Galileo by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/spans/:span_id`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Span](https://docs.galileo.ai/api-reference/trace/get-span)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
| `span_id` | path | `string` | yes | Galileo span UUID. |
