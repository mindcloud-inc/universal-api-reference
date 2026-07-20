# Update Checklist Item with Habitica

Updates a checklist item in Habitica.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:taskId/checklist/:itemId`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Update Checklist Item](https://habitica.com/apidoc/#api-Task-UpdateChecklistItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
| `itemId` | path | `string` | yes | The checklist item ID. |
| `text` | body | `string` | no | Updated checklist item text. |
