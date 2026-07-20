# Update Task with Follow Up Boss

Updates an existing task in Follow Up Boss.

## Endpoint

- **Method:** `PUT`
- **Path:** `tasks/:id`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [Update Task](https://docs.followupboss.com/reference/tasks-id-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The task ID. |
| `name` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `dueDate` | body | `date` | no | — |
| `assignedUserId` | body | `number` | no | — |
| `isCompleted` | body | `boolean` | no | — |
