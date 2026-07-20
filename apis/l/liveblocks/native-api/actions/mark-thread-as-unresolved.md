# Mark Thread As Unresolved with Liveblocks

Marks a thread as unresolved in Liveblocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/mark-as-unresolved`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Mark Thread As Unresolved](https://liveblocks.io/docs/api-reference/rest-api-endpoints#mark-thread-as-unresolved)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
