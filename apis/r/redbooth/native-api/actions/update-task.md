# Update Task with Redbooth

Updates an existing task in Redbooth.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Update Task](https://redbooth.com/api/api-docs/#page:tasks,header:tasks-task-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Redbooth task ID |
| `name` | body | `string` | no | Updated task name |
| `description` | body | `string` | no | Updated task description |
