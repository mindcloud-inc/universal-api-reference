# Delete Task Note with Checkvist

Deletes a task note from Checkvist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/checklists/:checklistId/tasks/:taskId/comments/:noteId.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Delete Task Note](https://checkvist.com/auth/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `noteId` | path | `number` | yes | The note ID. |
| `taskId` | path | `number` | yes | The task ID. |
