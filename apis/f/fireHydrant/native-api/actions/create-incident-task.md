# Create Incident Task with FireHydrant

Creates a new incident task in FireHydrant.

## Endpoint

- **Method:** `POST`
- **Path:** `/incidents/:incident_id/tasks`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [Create Incident Task](https://docs.firehydrant.com/reference/create_incident_task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignee_id` | body | `string` | no | The user ID assigned to the task. |
| `description` | body | `string` | no | Task description. |
| `due_at` | body | `string` | no | Task due date or relative time like 5m. |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
| `title` | body | `string` | yes | The task title. |
| `state` | body | `list` | no | Task state: open, in_progress, cancelled, or done. Accepted values: `0`, `1`, `2`, `3`. |
