# Send a LinkedIn message with ConnectSafely

**DEPRECATED: Use POST /conversations/send instead.** This endpoint still works but returns a `_deprecated` warning in the response body. The /conversations/send endpoint auto-detects Sales Navigator accounts, supports attachments, and handles both standard and Sales Nav messaging transparently. For attachments, upload each file via POST /conversations/upload-attachment (raw binary body; use an image/* content type to render images inline), then pass the returned attachment wrapped as { file: <attachment> }. --- Send a direct message to a LinkedIn member. Supports regular messages (requires 1st-degree connection) and InMail (for non-connections, requires Premium). Can also send messages in group context. **Either recipientProfileId or recipientProfileUrn must be provided.** **Rate limit: 100 messages per day per LinkedIn account.**

## Endpoint

- **Method:** `POST`
- **Path:** `/message`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send a LinkedIn message](https://connectsafely.ai/docs/api/linkedin-actions/post-message-send-message)

## Quota

100 messages per day per LinkedIn account (not per API key).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `recipientProfileId` | body | `string` | no | Recipient LinkedIn profile vanity URL slug (e.g., "john-doe-123"). Either this or recipientProfileUrn is required. Prefer recipientProfileUrn when available. |
| `recipientProfileUrn` | body | `string` | no | Recipient LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Either this or recipientProfileId is required. Preferred over recipientProfileId. |
| `message` | body | `string` | yes | Message content to send. Supports basic formatting. |
| `subject` | body | `string` | no | Subject line (required for InMail, optional for regular messages) |
| `messageType` | body | `list` | no | Message type: normal (1st-degree connections) or inmail (non-connections, requires Premium credits) Accepted values: `normal`, `inmail`. Default: `normal`. |
| `groupId` | body | `string` | no | Group ID to send message in group context (enables messaging non-connections who are group members) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` | Status message |
| `recipientProfileUrn` | `string` | LinkedIn URN of the recipient |

### Example response

```json
{
  "success": true,
  "message": "Message sent successfully",
  "recipientProfileUrn": "urn:li:fsd_profile:ACoAAA24A-MBVEvT49xpVF2gnWrhvmUIPDJshSM"
}
```

## Error status codes

`400`, `401`, `404`, `429`. Bodies follow the shared `{ success, code, message }` error shape.
