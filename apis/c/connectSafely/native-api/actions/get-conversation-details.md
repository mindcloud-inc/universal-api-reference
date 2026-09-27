# Get conversation details with ConnectSafely

**DEPRECATED: Use GET /conversations/{conversationUrn}/messages instead.** This endpoint now redirects (307) to the new conversations messages endpoint. The new endpoint provides DB-first caching, cursor pagination, sync mode, and auto-detects Sales Navigator threads. --- Retrieve detailed message history for a specific LinkedIn conversation. Supports pagination via deliveredAt timestamp to load older/newer messages. Returns full message content, sender info, and timestamps.

## Endpoint

- **Method:** `GET`
- **Path:** `/messaging/conversation-details`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get conversation details](https://connectsafely.ai/docs/api/linkedin-messaging/get-messaging-conversation-details-get-conversation-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `profileId` | query | `string` | no | Profile ID of conversation participant (optional) |
| `conversationUrn` | query | `string` | yes | LinkedIn conversation URN from recent-messages response |
| `deliveredAt` | query | `number` | no | Timestamp (milliseconds) for pagination anchor point |
| `countBefore` | query | `number` | no | Number of messages before deliveredAt timestamp |
| `countAfter` | query | `number` | no | Number of messages after deliveredAt timestamp |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` |  |
| `profileUrn` | `string` |  |
| `conversationUrn` | `string` |  |
| `messages` | `array` |  |
| `messages[].messageId` | `string` |  |
| `messages[].backendMessageUrn` | `string` |  |
| `messages[].text` | `string` |  |
| `messages[].subject` | `string` |  |
| `messages[].sentAt` | `number` |  |
| `messages[].sender` | `object` |  |
| `messages[].sender.profileId` | `string` |  |
| `messages[].sender.name` | `string` |  |
| `messages[].sender.profileUrl` | `string` |  |
| `messages[].sender.profilePicture` | `string` |  |
| `messages[].sender.participantUrn` | `string` |  |
| `messages[].attachments` | `array` |  |
| `messages[].reactions` | `array` |  |
| `messages[].hasAttachment` | `boolean` |  |
| `total` | `number` |  |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "profileUrn": "urn:li:fsd_profile:ACoAAATPlQ0Bc8wdg-Iy8wZgEDuSdIVWJiE1Aio",
  "conversationUrn": "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAATPlQ0Bc8wdg-Iy8wZgEDuSdIVWJiE1Aio,2-NzkzMDFlNzAtZjU2OS00MjIwLWE2ZDctYzZkMWE1ZDljZDAyXzEwMA==)",
  "messages": [
    {
      "messageId": "urn:li:msg_message:(urn:li:fsd_profile:ACoAAATPlQ0Bc8wdg-Iy8wZgEDuSdIVWJiE1Aio,2-MTc2MDc3MzMxMDQyOWI2OTc1NC0xMDA=)",
      "backendMessageUrn": "urn:li:messagingMessage:2-MTc2MDc3MzMxMDQyOWI2OTc1NC0xMDA=",
      "text": "Hello",
      "subject": null,
      "sentAt": 1760773310429,
      "sender": {
        "profileId": "ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
        "name": "Jane Smith",
        "profileUrl": "https://www.linkedin.com/in/ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
        "profilePicture": "https://media.licdn.com/dms/image/...",
        "participantUrn": "urn:li:msg_messagingParticipant:urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o"
      },
      "attachments": null,
      "reactions": null,
      "hasAttachment": false
    }
  ]
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
