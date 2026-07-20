# Create Task Note with Checkvist

Creates a task note in Checkvist.

## Endpoint

- **Method:** `POST`
- **Path:** `/checklists/:checklistId/tasks/:taskId/comments.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Create Task Note](https://checkvist.com/auth/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `comment.comment` | body | `string` | yes | The note text. |
| `taskId` | path | `number` | yes | The task ID. |
