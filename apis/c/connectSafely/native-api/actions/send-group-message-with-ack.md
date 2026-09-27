# Send group message with delivery acknowledgment with ConnectSafely

**DEPRECATED: Use POST /conversations/send instead.** --- Send a LinkedIn message using group context while acknowledging delivery of previous messages. Useful for group-based conversations where you want to track message delivery. Rate limit: 150 messages per day per account.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/send-group-with-ack`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send group message with delivery acknowledgment](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-group-with-ack-send-group-message-with-ack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `recipientProfileUrn` | body | `string` | yes | Recipient LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over recipientProfileId. |
| `groupId` | body | `string` | yes | LinkedIn group ID |
| `message` | body | `string` | yes | Message content to send |
| `messageUrns` | body | `array` | no | Message URNs to acknowledge |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `recipientProfileUrn` | `string` |  |
| `groupId` | `string` |  |
| `acknowledgmentSent` | `boolean` |  |

### Example response

```json
{
  "success": true,
  "message": "Group context message sent successfully",
  "recipientProfileUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
  "groupId": "12345678",
  "acknowledgmentSent": true
}
```

## Error status codes

`400`, `401`, `403`, `429`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
