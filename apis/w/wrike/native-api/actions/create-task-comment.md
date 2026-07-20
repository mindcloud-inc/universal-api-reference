# Create Task Comment with Wrike

Creates a new comment on a Wrike task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/comments`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [Create Task Comment](https://developers.wrike.com/api/v4/comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Wrike task ID where the comment will be created. |
| `text` | query | `string` | yes | Comment text, cannot be empty |
| `plainText` | query | `boolean` | no | Treat comment text as plain text |
