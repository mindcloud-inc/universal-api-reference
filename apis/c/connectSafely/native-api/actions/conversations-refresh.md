# Refresh conversation messages with ConnectSafely

Trigger background refresh of messages for a conversation. Results pushed via WebSocket.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/refresh`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Refresh conversation messages](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-refresh-conversations-refresh)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID |
| `conversationUrn` | body | `string` | yes | Conversation URN to refresh |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `conversationUrn` | `string` |  |
| `accountId` | `string` |  |

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
