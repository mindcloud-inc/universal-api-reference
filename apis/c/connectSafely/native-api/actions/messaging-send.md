# Send a message (messaging wrapper) with ConnectSafely

**DEPRECATED: Use POST /conversations/send instead.** The /conversations/send endpoint auto-detects Sales Navigator accounts, supports attachments, and handles both standard and Sales Nav messaging transparently. --- Send a LinkedIn message using the messaging endpoint. Wrapper around the core messaging functionality with a cleaner interface. Supports regular messages and InMail. Rate limit: 150 messages per day per account.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/send`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send a message (messaging wrapper)](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-messaging-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `recipientProfileId` | body | `string` | no | Recipient LinkedIn profile vanity URL slug (e.g., "john-doe-123"). Prefer recipientProfileUrn when available. |
| `recipientProfileUrn` | body | `string` | no | Recipient LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over recipientProfileId. |
| `message` | body | `string` | yes | Message content to send |
| `subject` | body | `string` | no | Subject line (required for InMail) |
| `messageType` | body | `list` | no | Message type Accepted values: `normal`, `inmail`. Default: `normal`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `recipientProfileUrn` | `string` |  |

### Example response

```json
{
  "success": true,
  "message": "Message sent successfully",
  "recipientProfileUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o"
}
```

## Error status codes

`400`, `401`, `429`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
