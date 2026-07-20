# Update Task with Trackabi

Updates an existing task in Trackabi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/tasks/:taskId`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [Update Task](https://trackabi.com/help/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `number` | yes | The unique ID of the task. |
| `name` | body | `string` | no | Task name. |
| `description` | body | `string` | no | Task description. |
| `parent_task_id` | body | `number` | no | Parent task. |
| `estimated_time` | body | `string` | no | Estimated time. |
| `start_date` | body | `date` | no | Task start date. |
| `end_date` | body | `date` | no | Task end date. |
| `not_billable` | body | `number` | no | Flag indicating whether the task is billable. |
