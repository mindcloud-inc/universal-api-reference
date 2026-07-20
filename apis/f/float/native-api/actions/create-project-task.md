# Create Project Task with Float

Creates a new project task in Float.

## Endpoint

- **Method:** `POST`
- **Path:** `/project-tasks`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Create Project Task](https://developer.float.com/api_reference.html#Project_Tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phase_id` | body | `number` | no | The ID of the phase the project task belongs to |
| `project_id` | body | `number` | yes | The ID of the project the project task belongs to |
| `task_name` | body | `string` | yes | The name of the project task |
