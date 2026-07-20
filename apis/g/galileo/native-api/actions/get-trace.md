# Get Trace with Galileo

Retrieves a trace from Galileo by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/traces/:trace_id`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Trace](https://docs.galileo.ai/api-reference/trace/get-trace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
| `trace_id` | path | `string` | yes | Galileo trace UUID. |
