# Mark conversation as seen with ConnectSafely

**DEPRECATED: Will be moved to /conversations API.** --- Mark a LinkedIn conversation as seen/read. This updates the read status for the sender and removes the unread indicator. Useful for managing inbox state programmatically.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/mark-seen`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Mark conversation as seen](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-mark-seen-mark-conversation-seen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `conversationUrn` | body | `string` | yes | LinkedIn conversation URN to mark as seen |

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
  "message": "Conversation marked as seen successfully"
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
