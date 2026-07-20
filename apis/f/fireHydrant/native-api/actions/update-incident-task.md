# Update Incident Task with FireHydrant

Updates an existing incident task in FireHydrant.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/incidents/:incident_id/tasks/:task_id`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [Update Incident Task](https://docs.firehydrant.com/reference/update_incident_task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignee_id` | body | `string` | no | The user ID assigned to the task. |
| `description` | body | `string` | no | Task description. |
| `due_at` | body | `string` | no | Task due date or relative time like 5m. |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
| `title` | body | `string` | no | The task title. |
| `task_id` | path | `string` | yes | The FireHydrant incident task ID. |
| `state` | body | `list` | no | Task state: open, in_progress, cancelled, or done. Accepted values: `0`, `1`, `2`, `3`. |
