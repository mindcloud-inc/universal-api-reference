# Update Task with Insightful

Updates an existing task in your Insightful account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/task/:id`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Update Task](https://developers.insightful.io/#f0ebc231-a938-4679-a6ce-940cc137cb7a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billable` | body | `boolean` | no | Whether the task is billable. |
| `deadline` | body | `number` | no | Task deadline in milliseconds. |
| `description` | body | `string` | no | The updated task description. |
| `employees[]` | body | `array<string>` | no | Employee IDs assigned to the task. |
| `id` | path | `string` | yes | The task ID to update. |
| `name` | body | `string` | no | The updated task name. |
| `status` | body | `string` | no | The updated task status. |
