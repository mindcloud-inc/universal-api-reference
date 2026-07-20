# Update Task with Nozbe Personal

Updates an existing task in Nozbe Personal.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Update Task](https://api4.nozbe.com/v1/api#/tasks/putTaskById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID to update. |
| `name` | body | `string` | no | Updated task name. |
