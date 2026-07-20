# Score Checklist Item with Habitica

Scores a checklist item in Habitica.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/checklist/:itemId/score`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Score Checklist Item](https://habitica.com/apidoc/#api-Task-ScoreChecklistItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Habitica task ID. |
| `itemId` | path | `string` | yes | The checklist item ID. |
