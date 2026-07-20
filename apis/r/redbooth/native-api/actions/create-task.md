# Create Task with Redbooth

Creates a new task in Redbooth.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Create Task](https://redbooth.com/api/api-docs/#page:tasks,header:tasks-task-list-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Task name |
| `task_list_id` | body | `number` | yes | Target Redbooth task list ID |
| `description` | body | `string` | no | Task description |
