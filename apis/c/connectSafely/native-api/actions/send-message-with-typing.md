# Send message with typing indicator with ConnectSafely

**DEPRECATED: Use POST /conversations/send instead.** --- Send a LinkedIn message after showing a typing indicator first. Creates a more natural conversation experience by simulating human-like behavior. Requires conversationUrn for existing conversations. Rate limit: 150 messages per day per account.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/send-with-typing`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send message with typing indicator](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-with-typing-send-message-with-typing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `recipientProfileId` | body | `string` | no | Recipient LinkedIn profile vanity URL slug (e.g., "john-doe-123"). Prefer recipientProfileUrn when available. |
| `recipientProfileUrn` | body | `string` | no | Recipient LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over recipientProfileId. |
| `message` | body | `string` | yes | Message content to send |
| `subject` | body | `string` | no | Subject line (for InMail) |
| `messageType` | body | `list` | no | Message type Accepted values: `normal`, `inmail`. Default: `normal`. |
| `conversationUrn` | body | `string` | no | Conversation URN (required for typing indicator in existing conversations) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `recipientProfileUrn` | `string` |  |
| `typingIndicatorSent` | `boolean` |  |

### Example response

```json
{
  "success": true,
  "message": "Message sent successfully",
  "recipientProfileUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
  "typingIndicatorSent": true
}
```

## Error status codes

`400`, `401`, `429`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
