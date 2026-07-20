# Update Task with ProProfs Project

Updates an existing task in ProProfs Project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/{{task_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Task](https://help.proprofsproject.com/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The updated task description. |
| `task_id` | path | `string` | yes | The task ID to update. |
| `task_name` | body | `string` | no | The updated task name. |
