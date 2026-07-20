# Get Thread Subscriptions with Liveblocks

Retrieves thread subscriptions from Liveblocks.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:roomId/threads/:threadId/subscriptions`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Get Thread Subscriptions](https://liveblocks.io/docs/api-reference/rest-api-endpoints#get-thread-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | no | ID of the room. |
| `threadId` | path | `string` | no | ID of the thread. |
