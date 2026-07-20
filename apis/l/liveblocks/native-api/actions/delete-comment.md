# Delete Comment with Liveblocks

Deletes an existing comment from Liveblocks.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rooms/:roomId/threads/:threadId/comments/:commentId`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Delete Comment](https://liveblocks.io/docs/api-reference/rest-api-endpoints#delete-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | no | ID of the comment. |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
