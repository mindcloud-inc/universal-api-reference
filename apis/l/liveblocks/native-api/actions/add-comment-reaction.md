# Add Comment Reaction with Liveblocks

Creates a comment reaction in Liveblocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/comments/:commentId/add-reaction`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Add Comment Reaction](https://liveblocks.io/docs/api-reference/rest-api-endpoints#add-comment-reaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | no | ID of the comment. |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
