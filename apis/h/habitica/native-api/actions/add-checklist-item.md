# Add Checklist Item with Habitica

Adds a checklist item to a Habitica task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/checklist`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Add Checklist Item](https://habitica.com/apidoc/#api-Task-AddChecklistItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
| `text` | body | `string` | yes | Checklist item text. |
