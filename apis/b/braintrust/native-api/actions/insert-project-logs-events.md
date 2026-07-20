# Insert Project Logs Events with Braintrust

Creates project log events in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/project_logs/:project_id/insert`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Insert Project Logs Events](https://braintrust.dev/docs/api-reference/logs/insert-project-logs-events.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id. |
| `events[]` | body | `array<object>` | yes | Events to insert. |
