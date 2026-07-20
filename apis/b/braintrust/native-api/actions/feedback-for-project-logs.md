# Feedback For Project Logs with Braintrust

Creates feedback for project log events in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/project_logs/:project_id/feedback`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Feedback For Project Logs](https://braintrust.dev/docs/api-reference/logs/feedback-for-project-logs-events.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id. |
| `feedback[]` | body | `array<object>` | yes | Feedback items. |
