# Delete Task with Habitica

Deletes an existing task from Habitica.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Delete Task](https://habitica.com/apidoc/#api-Task-DeleteTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
