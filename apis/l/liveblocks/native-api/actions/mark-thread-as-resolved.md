# Mark Thread As Resolved with Liveblocks

Marks a thread as resolved in Liveblocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/mark-as-resolved`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Mark Thread As Resolved](https://liveblocks.io/docs/api-reference/rest-api-endpoints#mark-thread-as-resolved)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
