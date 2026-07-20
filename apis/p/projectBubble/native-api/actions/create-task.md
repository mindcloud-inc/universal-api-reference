# Create Task with Project Bubble

Creates a new task in a Project Bubble project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:project_id`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Task](https://help.proprofsproject.com/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The parent project ID for the new task. |
| `task_name` | body | `string` | yes | The name of the task to create. |
