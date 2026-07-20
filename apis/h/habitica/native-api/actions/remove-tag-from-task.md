# Remove Tag From Task with Habitica

Removes a tag from a Habitica task.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId/tags/:tagId`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Remove Tag From Task](https://habitica.com/apidoc/#api-Task-RemoveTagFromTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
| `tagId` | path | `string` | yes | The Habitica tag ID. |
