# Update Task with Quire

Updates an existing task in Quire.

## Endpoint

- **Method:** `PUT`
- **Path:** `task/id/:projectId/:id`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Update Task](https://quire.io/dev/api/#operation--task-id--projectId---id--put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID or shortcut, for example App_Account. |
| `id` | path | `number` | yes | The numeric task ID. |
| `name` | body | `string` | no | Optional updated task title. |
| `description` | body | `string` | no | Optional updated task description in Markdown. |
