# Delete manual time entry with KanbanFlow

Deletes an existing manual time entry from KanbanFlow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId/manual-time-entries/:manualTimeEntryId`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Delete manual time entry](https://kanbanflow.com/api-docs/delete-manual-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `manualTimeEntryId` | path | `string` | yes | The KanbanFlow manual time entry ID. |
