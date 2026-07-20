# Create Task Comment with Awork

Creates a task comment in Awork.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/comments`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Create Task Comment](https://developers.awork.com/apiv1/task-comments/post-task-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The id of the task. |
| `message` | body | `string` | yes | The message of the comment. |
| `previews` | body | `string` | no | The preview URLs to show a preview for. Send multiple values as a array. |
| `inReplyToCommentId` | body | `string` | no | The parent comment this comment replies to. |
| `userId` | body | `string` | no | The id of the user who created the comment. If omitted, Awork defaults to the current user. |
| `isHiddenForConnectUsers` | body | `boolean` | no | Whether the comment is hidden for connect users. If omitted, Awork keeps the default visible behavior. |
