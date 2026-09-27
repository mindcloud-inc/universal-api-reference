# Send message with group context with ConnectSafely

Send a LinkedIn message to someone using group membership context. Allows messaging non-connections who are members of the same LinkedIn group without using InMail credits. Rate limit: 150 messages per day per account.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/send-group`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send message with group context](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-send-group-send-group-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `recipientProfileUrn` | body | `string` | yes | Recipient LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over recipientProfileId. |
| `groupId` | body | `string` | yes | LinkedIn group ID that both sender and recipient are members of |
| `message` | body | `string` | yes | Message content to send |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `recipientProfileUrn` | `string` |  |
| `groupId` | `string` |  |

### Example response

```json
{
  "success": true,
  "message": "Group context message sent successfully",
  "recipientProfileUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
  "groupId": "12345678"
}
```

## Error status codes

`400`, `401`, `403`, `429`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
