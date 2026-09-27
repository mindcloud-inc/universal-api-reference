# Get recent messages with ConnectSafely

**DEPRECATED: Use GET /conversations instead.** This endpoint now redirects (307) to GET /conversations. The /conversations endpoint provides DB-first caching, multi-account support, and automatic Sales Navigator thread merging. --- Retrieve recent LinkedIn messages/conversations for the authenticated account. Supports filtering by keywords and read status. Returns simplified conversation list with latest message preview. Rate limit: 150 messages per day per account.

## Endpoint

- **Method:** `GET`
- **Path:** `/messaging/recent-messages`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get recent messages](https://connectsafely.ai/docs/api/linkedin-messaging/get-messaging-recent-messages-get-recent-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `nextCursor` | query | `string` | no | Cursor for pagination from previous response |
| `count` | query | `number` | no | Number of conversations to return |
| `keywords` | query | `string` | no | Search keywords to filter conversations |
| `read` | query | `string` | no | Filter by read status: "true" or "false" |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` |  |
| `profileUrn` | `string` |  |
| `conversations` | `array` |  |
| `conversations[].conversationId` | `string` |  |
| `conversations[].conversationUrn` | `string` |  |
| `conversations[].backendConversationUrn` | `string` |  |
| `conversations[].conversationUrl` | `string` |  |
| `conversations[].participants` | `array` |  |
| `conversations[].participants[].profileId` | `string` |  |
| `conversations[].participants[].name` | `string` |  |
| `conversations[].participants[].headline` | `string` |  |
| `conversations[].participants[].profileUrl` | `string` |  |
| `conversations[].participants[].profilePicture` | `string` |  |
| `conversations[].participants[].distance` | `string` |  |
| `conversations[].participants[].memberBadgeType` | `string` |  |
| `conversations[].participants[].participantUrn` | `string` |  |
| `conversations[].participants[].backendUrn` | `string` |  |
| `conversations[].participants[].hostIdentityUrn` | `string` |  |
| `conversations[].unreadCount` | `number` |  |
| `conversations[].lastActivityAt` | `number` |  |
| `conversations[].createdAt` | `number` |  |
| `conversations[].lastReadAt` | `number` |  |
| `conversations[].isRead` | `boolean` |  |
| `conversations[].state` | `string` |  |
| `conversations[].latestMessage` | `object` |  |
| `conversations[].latestMessage.messageUrn` | `string` |  |
| `conversations[].latestMessage.backendMessageUrn` | `string` |  |
| `conversations[].latestMessage.text` | `string` |  |
| `conversations[].latestMessage.sentAt` | `number` |  |
| `conversations[].latestMessage.senderName` | `string` |  |
| `conversations[].latestMessage.senderProfileUrl` | `string` |  |
| `conversations[].latestMessage.senderUrn` | `string` |  |
| `conversations[].latestMessage.hasAttachment` | `boolean` |  |
| `total` | `number` |  |
| `nextCursor` | `string` |  |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "profileUrn": "urn:li:fsd_profile:ACoAAATPlQ0Bc8wdg-Iy8wZgEDuSdIVWJiE1Aio",
  "conversations": [
    {
      "conversationId": "2-ODFkYjU4M2ItZDlmYS00YTVjLThlNTQtZjI5YTE4ZWUyZDk5XzEwMA==",
      "conversationUrn": "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAATPlQ0Bc8wdg-Iy8wZgEDuSdIVWJiE1Aio,2-ODFkYjU4M2ItZDlmYS00YTVjLThlNTQtZjI5YTE4ZWUyZDk5XzEwMA==)",
      "backendConversationUrn": "urn:li:messagingThread:2-ODFkYjU4M2ItZDlmYS00YTVjLThlNTQtZjI5YTE4ZWUyZDk5XzEwMA==",
      "conversationUrl": "https://www.linkedin.com/messaging/thread/2-ODFkYjU4M2ItZDlmYS00YTVjLThlNTQtZjI5YTE4ZWUyZDk5XzEwMA==/",
      "participants": [
        {
          "profileId": "ACoAADSoo60BM6hxemTbnN2aA_Z1-WlNFRhRYhU",
          "name": "John Doe",
          "headline": "Software Engineer at Tech Company",
          "profileUrl": "https://www.linkedin.com/in/ACoAADSoo60BM6hxemTbnN2aA_Z1-WlNFRhRYhU",
          "profilePicture": "https://media.licdn.com/dms/image/...",
          "distance": "DISTANCE_1",
          "memberBadgeType": null,
          "participantUrn": "urn:li:msg_messagingParticipant:urn:li:fsd_profile:ACoAADSoo60BM6hxemTbnN2aA_Z1-WlNFRhRYhU",
          "backendUrn": "urn:li:member:883467181",
          "hostIdentityUrn": "urn:li:fsd_profile:ACoAADSoo60BM6hxemTbnN2aA_Z1-WlNFRhRYhU"
        }
      ],
      "unreadCount": 0,
      "lastActivityAt": 1771950346603,
      "createdAt": 1771317337868,
      "lastReadAt": 1771950726332,
      "isRead": true,
      "state": null,
      "latestMessage": {
        "messageUrn": "urn:li:msg_message:(urn:li:fsd_profile:ACoAAATPlQ0Bc8wdg-Iy8wZgEDuSdIVWJiE1Aio,2-MTc3MTk1MDM0NjYwM2I5NzY0NS0xMDA=)",
        "backendMessageUrn": "urn:li:messagingMessage:2-MTc3MTk1MDM0NjYwM2I5NzY0NS0xMDA=",
        "text": "Hello, how are you?",
        "sentAt": 1771950346603,
        "senderName": "John Doe",
        "senderProfileUrl": "https://www.linkedin.com/in/ACoAADSoo60BM6hxemTbnN2aA_Z1-WlNFRhRYhU",
        "senderUrn": "urn:li:msg_messagingParticipant:urn:li:fsd_profile:ACoAADSoo60BM6hxemTbnN2aA_Z1-WlNFRhRYhU",
        "hasAttachment": false
      }
    }
  ]
}
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
