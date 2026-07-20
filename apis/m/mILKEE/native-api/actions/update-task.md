# Update Task with MILKEE

Updates an existing task in MILKEE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:companyId/tasks/:taskId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Update Task](https://apidocs.milkee.ch/api/resources/tasks.html#update-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `description` | body | `string` | no | Task description. |
| `due` | body | `string` | no | Task due date. |
| `planned_hours` | body | `number` | no | Estimated hours to complete the task. |
| `project_id` | body | `number` | no | ID of the project this task belongs to. |
| `status` | body | `string` | no | Task status: open, in-progress, or done. |
| `task_id` | path | `string` | yes | The numeric MILKEE task ID used in the request path. |
| `title` | body | `string` | no | Task title. |
