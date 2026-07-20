# Update Task with Paymo

Updates an existing task in Paymo.

## Endpoint

- **Method:** `PUT`
- **Path:** `tasks/:taskId`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [Update Task](https://github.com/paymo-org/api/blob/master/sections/tasks.md#updating-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | The Paymo task id. |
| `name` | body | `string` | no | Updated task name. |
| `description` | body | `string` | no | Updated task description. |
