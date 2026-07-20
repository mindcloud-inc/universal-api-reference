# Update Task with Nozbe Teams

Updates an existing task in Nozbe Teams.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Update Task](https://api4.nozbe.com/v1/api#/tasks/putTaskById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The task to update. |
| `name` | body | `string` | no | The updated task name. |
