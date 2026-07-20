# Create Task with ProProfs Project

Creates a new task in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/{{project_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Task](https://help.proprofsproject.com/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The task description. |
| `project_id` | path | `string` | yes | The parent project ID. |
| `task_name` | body | `string` | yes | The task name. |
