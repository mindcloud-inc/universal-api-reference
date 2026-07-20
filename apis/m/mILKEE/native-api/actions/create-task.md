# Create Task with MILKEE

Creates a new task in MILKEE.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/tasks`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Create Task](https://apidocs.milkee.ch/api/resources/tasks.html#create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `description` | body | `string` | no | Task description. |
| `due` | body | `string` | yes | Task due date. |
| `planned_hours` | body | `number` | no | Estimated hours to complete the task. |
| `project_id` | body | `number` | yes | ID of the project this task belongs to. |
| `status` | body | `string` | no | Task status: open, in-progress, or done. |
| `title` | body | `string` | yes | Task title. |
