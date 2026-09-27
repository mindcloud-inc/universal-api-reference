# React or unreact to a message with ConnectSafely

Add or remove an emoji reaction on a message. The reaction is applied on LinkedIn first; other connected clients/tabs are notified via WebSocket. Set react=true to add the reaction, react=false to remove it.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversationUrn/messages/:messageUrn/react`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [React or unreact to a message](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-conversationurn-messages-messageurn-react-conversations-react-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationUrn` | param | `string` | yes | Conversation URN (URL-encoded) |
| `messageUrn` | param | `string` | yes | URN of the message to react to (URL-encoded) |
| `accountId` | query | `string` | no | LinkedIn account ID |
| `emoji` | body | `string` | yes | Emoji to react with (e.g., "👍") |
| `react` | body | `boolean` | yes | true to add the reaction, false to remove it |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `messageUrn` | `string` |  |
| `emoji` | `string` |  |
| `react` | `boolean` |  |

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
