# Add Tag To Task with Habitica

Adds a tag to a Habitica task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/tags/:tagId`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Add Tag To Task](https://habitica.com/apidoc/#api-Task-AddTagToTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
| `tagId` | path | `string` | yes | The Habitica tag ID. |
