# Subscribe To Thread with Liveblocks

Updates a Liveblocks thread subscription by subscribing a user.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/subscribe`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Subscribe To Thread](https://liveblocks.io/docs/api-reference/rest-api-endpoints#subscribe-to-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
