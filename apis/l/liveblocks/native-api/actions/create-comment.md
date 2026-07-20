# Create Comment with Liveblocks

Creates a new comment in Liveblocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/comments`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Create Comment](https://liveblocks.io/docs/api-reference/rest-api-endpoints#create-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
