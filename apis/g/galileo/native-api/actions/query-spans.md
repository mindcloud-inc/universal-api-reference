# Query Spans with Galileo

Finds spans in a Galileo project by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects/:project_id/spans/search`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Query Spans](https://docs.galileo.ai/api-reference/trace/query-spans)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
| `log_stream_id` | body | `string` | no | Optional Galileo log stream UUID. Provide exactly one of Log Stream ID, Experiment ID, or Metrics Testing ID. |
| `experiment_id` | body | `string` | no | Optional Galileo experiment UUID. Provide exactly one of Log Stream ID, Experiment ID, or Metrics Testing ID. |
