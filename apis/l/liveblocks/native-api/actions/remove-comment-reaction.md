# Remove Comment Reaction with Liveblocks

Deletes a comment reaction from Liveblocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/comments/:commentId/remove-reaction`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Remove Comment Reaction](https://liveblocks.io/docs/api-reference/rest-api-endpoints#remove-comment-reaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | no | ID of the comment. |
| `emoji` | body | `string` | no | — |
| `removedAt` | body | `string` | no | — |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
| `userId` | body | `string` | no | — |
