# Edit Comment with Liveblocks

Updates an existing comment in Liveblocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/comments/:commentId`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Edit Comment](https://liveblocks.io/docs/api-reference/rest-api-endpoints#edit-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | no | ID of the comment. |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
