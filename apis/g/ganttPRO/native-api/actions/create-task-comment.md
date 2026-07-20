# Create Task Comment with GanttPRO

Creates a new comment on a GanttPRO task.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Create Task Comment](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | body | `number` | yes | Task identifier for the new comment. |
| `userId` | body | `number` | yes | User identifier for the comment author. |
| `content` | body | `string` | yes | Comment content. |
