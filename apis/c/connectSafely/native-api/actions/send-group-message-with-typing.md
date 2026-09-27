# Send group message with typing indicator with ConnectSafely

**DEPRECATED: Use POST /conversations/send instead.** --- Send a LinkedIn message using group context after showing a typing indicator. Combines group messaging capability with natural typing simulation. Rate limit: 150 messages per day per account.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/send-group-with-typing`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send group message with typing indicator](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-group-with-typing-send-group-message-with-typing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `recipientProfileUrn` | body | `string` | yes | Recipient LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over recipientProfileId. |
| `groupId` | body | `string` | yes | LinkedIn group ID |
| `message` | body | `string` | yes | Message content to send |
| `conversationUrn` | body | `string` | no | Conversation URN for existing conversations |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `recipientProfileUrn` | `string` |  |
| `groupId` | `string` |  |
| `typingIndicatorSent` | `boolean` |  |

### Example response

```json
{
  "success": true,
  "message": "Group context message sent successfully",
  "recipientProfileUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
  "groupId": "12345678",
  "typingIndicatorSent": true
}
```

## Error status codes

`400`, `401`, `403`, `429`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
