# Send typing indicator with ConnectSafely

**DEPRECATED: Will be moved to /conversations API.** --- Send a typing indicator to a LinkedIn conversation. Shows the recipient that you are typing a message. Useful for creating a more natural conversation experience before sending a message.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/typing-indicator`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send typing indicator](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-typing-indicator-send-typing-indicator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `conversationUrn` | body | `string` | yes | LinkedIn conversation URN to send typing indicator to |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` |  |
| `conversationUrn` | `string` |  |
| `message` | `string` |  |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "conversationUrn": "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAATPlQ0Bc8wdg-Iy8wZgEDuSdIVWJiE1Aio,2-NzkzMDFlNzAtZjU2OS00MjIwLWE2ZDctYzZkMWE1ZDljZDAyXzEwMA==)",
  "message": "Typing indicator sent successfully"
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
