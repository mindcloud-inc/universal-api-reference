# Update manual time entry with KanbanFlow

Updates an existing manual time entry in KanbanFlow.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/manual-time-entries/:manualTimeEntryId`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Update manual time entry](https://kanbanflow.com/api-docs/update-manual-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `manualTimeEntryId` | path | `string` | yes | The KanbanFlow manual time entry ID. |
| `startTimestamp` | body | `string` | no | The UTC timestamp when the entry started. |
| `endTimestamp` | body | `string` | no | The UTC timestamp when the entry ended. |
| `comment` | body | `string` | no | A short comment for the time entry. Maximum length: 50. |
