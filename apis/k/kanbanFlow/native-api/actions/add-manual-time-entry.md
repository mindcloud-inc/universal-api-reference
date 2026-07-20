# Add manual time entry with KanbanFlow

Creates a new manual time entry in KanbanFlow.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/manual-time-entries`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Add manual time entry](https://kanbanflow.com/api-docs/add-manual-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `startTimestamp` | body | `string` | yes | The UTC timestamp when the entry started. |
| `endTimestamp` | body | `string` | yes | The UTC timestamp when the entry ended. |
| `comment` | body | `string` | no | A short comment for the time entry. Maximum length: 50. |
