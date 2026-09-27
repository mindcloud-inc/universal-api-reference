# Send message with delivery acknowledgment with ConnectSafely

**DEPRECATED: Use POST /conversations/send instead.** --- Send a LinkedIn message while acknowledging receipt of previous messages. Useful for replying to conversations where you want to mark received messages as acknowledged. Rate limit: 150 messages per day per account.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/send-with-ack`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send message with delivery acknowledgment](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-with-ack-send-message-with-ack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `recipientProfileId` | body | `string` | no | Recipient LinkedIn profile vanity URL slug (e.g., "john-doe-123"). Prefer recipientProfileUrn when available. |
| `recipientProfileUrn` | body | `string` | no | Recipient LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over recipientProfileId. |
| `message` | body | `string` | yes | Message content to send |
| `subject` | body | `string` | no | Subject line (for InMail) |
| `messageType` | body | `list` | no | Message type Accepted values: `normal`, `inmail`. Default: `normal`. |
| `messageUrns` | body | `array` | no | Message URNs to acknowledge delivery of |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `recipientProfileUrn` | `string` |  |
| `acknowledgmentSent` | `boolean` |  |

### Example response

```json
{
  "success": true,
  "message": "Message sent successfully",
  "recipientProfileUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
  "acknowledgmentSent": false
}
```

## Error status codes

`400`, `401`, `429`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
