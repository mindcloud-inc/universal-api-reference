# Get Comment with Liveblocks

Retrieves a comment from Liveblocks.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:roomId/threads/:threadId/comments/:commentId`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Get Comment](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | no | ID of the comment. |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
