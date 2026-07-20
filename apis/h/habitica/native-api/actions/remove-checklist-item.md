# Remove Checklist Item with Habitica

Deletes a checklist item from Habitica.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId/checklist/:itemId`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Remove Checklist Item](https://habitica.com/apidoc/#api-Task-RemoveChecklistItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
| `itemId` | path | `string` | yes | The checklist item ID. |
