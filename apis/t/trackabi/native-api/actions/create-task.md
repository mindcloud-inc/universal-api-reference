# Create Task with Trackabi

Creates a new task in a Trackabi project.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects/:projectId/tasks`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [Create Task](https://trackabi.com/help/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The unique ID of the project. |
| `name` | body | `string` | yes | Task name. |
| `description` | body | `string` | no | Task description. |
| `parent_task_id` | body | `number` | no | Parent task. |
| `estimated_time` | body | `string` | no | Estimated time. |
| `start_date` | body | `date` | no | Task start date. |
| `end_date` | body | `date` | no | Task end date. |
| `not_billable` | body | `number` | no | Flag indicating whether the task is billable. |
