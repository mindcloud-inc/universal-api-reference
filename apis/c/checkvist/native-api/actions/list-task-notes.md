# List Task Notes with Checkvist

Retrieves task notes from Checkvist.

## Endpoint

- **Method:** `GET`
- **Path:** `/checklists/:checklistId/tasks/:taskId/comments.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [List Task Notes](https://checkvist.com/auth/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `taskId` | path | `number` | yes | The task ID. |
