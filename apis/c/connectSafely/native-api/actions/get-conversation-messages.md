# Get conversation messages with ConnectSafely

Retrieve messages for a specific conversation. Auto-detects Sales Navigator thread URNs (urn:li:salesNav_thread:*) and routes to the Sales Nav API. Standard conversations use DB-first with LinkedIn API fallback for older messages via cursor pagination. Replaces GET /messaging/conversation-details.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/:conversationUrn/messages`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get conversation messages](https://connectsafely.ai/docs/api/linkedin-messaging/get-conversations-conversationurn-messages-get-conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationUrn` | param | `string` | yes | Conversation URN (URL-encoded) |
| `accountId` | query | `string` | no | LinkedIn account ID |
| `count` | query | `number` | no | Number of messages Default: `50`. |
| `cursor` | query | `string` | no | Timestamp cursor for older messages |
| `since` | query | `number` | no | Timestamp to fetch messages newer than (polling) |
| `sync` | query | `boolean` | no | Wait for LinkedIn response (sync mode) Default: `True`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `messages` | `array` |  |
| `messages[].messageUrn` | `string` |  |
| `messages[].text` | `string` |  |
| `messages[].sentAt` | `number` |  |
| `messages[].senderProfileId` | `string` |  |
| `messages[].senderName` | `string` |  |
| `messages[].senderPhoto` | `string` |  |
| `messages[].isSentByOwner` | `boolean` |  |
| `messages[].hasAttachment` | `boolean` |  |
| `messages[].attachments` | `array` |  |
| `participants` | `array` |  |
| `participants[].profileId` | `string` |  |
| `participants[].name` | `string` |  |
| `participants[].headline` | `string` |  |
| `participants[].profilePicture` | `string` |  |
| `hasMore` | `boolean` |  |
| `cursor` | `string` |  |
| `note` | `string` |  |

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
