# Unsubscribe From Thread with Liveblocks

Updates a Liveblocks thread subscription by unsubscribing a user.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/unsubscribe`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Unsubscribe From Thread](https://liveblocks.io/docs/api-reference/rest-api-endpoints#unsubscribe-from-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
