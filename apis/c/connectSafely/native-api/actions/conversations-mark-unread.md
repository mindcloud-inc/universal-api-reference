# Mark a conversation as unread with ConnectSafely

Mark a conversation as unread on LinkedIn (source of truth) and locally. The account is resolved from the conversation, so no accountId is required. Other connected clients/tabs are notified via WebSocket.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conversations/:conversationUrn/mark-unread`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Mark a conversation as unread](https://connectsafely.ai/docs/api/linkedin-messaging/patch-conversations-conversationurn-mark-unread-conversations-mark-unread)

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
