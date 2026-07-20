# Update Task Note with Checkvist

Updates a task note in Checkvist.

## Endpoint

- **Method:** `PUT`
- **Path:** `/checklists/:checklistId/tasks/:taskId/comments/:noteId.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Update Task Note](https://checkvist.com/auth/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `comment.comment` | body | `string` | yes | The updated note text. |
| `noteId` | path | `number` | yes | The note ID. |
| `taskId` | path | `number` | yes | The task ID. |
