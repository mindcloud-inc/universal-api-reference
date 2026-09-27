# Star a conversation with ConnectSafely

Add LinkedIn's STARRED category to a conversation (synced to LinkedIn first as the source of truth) and persist it locally. The account is resolved from the conversation. Other connected clients/tabs are notified via WebSocket.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conversations/:conversationUrn/star`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Star a conversation](https://connectsafely.ai/docs/api/linkedin-messaging/patch-conversations-conversationurn-star-conversations-star)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationUrn` | param | `string` | yes | Conversation URN (URL-encoded) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `conversationUrn` | `string` |  |

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
