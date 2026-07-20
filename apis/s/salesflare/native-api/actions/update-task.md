# Update Task with Salesflare

## Endpoint

- **Method:** `PUT`
- **Path:** `tasks/:id`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [Update Task](https://api.salesflare.com/docs#/Tasks/putTasksId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `completed` | body | `boolean` | no | Whether the task is completed. |
| `description` | body | `string` | no | The task description. |
| `id` | path | `number` | yes | The Salesflare task ID. |
