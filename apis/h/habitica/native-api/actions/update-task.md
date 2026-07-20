# Update Task with Habitica

Updates an existing task in Habitica.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Update Task](https://habitica.com/apidoc/#api-Task-UpdateTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
| `text` | body | `string` | no | Updated task title. |
