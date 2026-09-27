# List conversations with ConnectSafely

List recent LinkedIn conversations using DB-first approach with LinkedIn API fallback. Supports multi-account batch queries, label/unread filtering. Auto-detects Sales Navigator accounts and merges Sales Nav threads with standard conversations.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [List conversations](https://connectsafely.ai/docs/api/linkedin-messaging/get-conversations-list-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | Single LinkedIn account ID |
| `linkedinAccountIds` | query | `string` | no | Comma-separated account IDs for multi-account batch |
| `count` | query | `number` | no | Number of conversations Default: `20`. |
| `nextCursor` | query | `string` | no | Pagination cursor (prefixed "linkedin:" for API pagination) |
| `labelId` | query | `string` | no | Filter by label ID |
| `labeledOnly` | query | `boolean` | no | Only labeled conversations |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `conversations` | `array` |  |
| `conversations[].conversationUrn` | `string` |  |
| `conversations[].conversationId` | `string` |  |
| `conversations[].lastActivityAt` | `date` |  |
| `conversations[].unreadCount` | `number` |  |
| `conversations[].participants` | `array` |  |
| `conversations[].participants[].profileId` | `string` |  |
| `conversations[].participants[].name` | `string` |  |
| `conversations[].participants[].headline` | `string` |  |
| `conversations[].participants[].profileUrl` | `string` |  |
| `conversations[].participants[].profilePicture` | `string` |  |
| `conversations[].participants[].distance` | `string` |  |
| `conversations[].latestMessage` | `object` |  |
| `conversations[].latestMessage.text` | `string` |  |
| `conversations[].latestMessage.sentAt` | `number` |  |
| `conversations[].latestMessage.senderName` | `string` |  |
| `conversations[].latestMessage.hasAttachment` | `boolean` |  |
| `conversations[].source` | `list` | Source of the conversation (sales_navigator for Sales Nav threads) |
| `conversations[].salesNavThreadId` | `string` | Sales Navigator thread ID (only for Sales Nav conversations) |
| `accounts` | `array` |  |
| `accounts[].id` | `string` |  |
| `accounts[].name` | `string` |  |
| `nextCursor` | `string` |  |
| `hasMore` | `boolean` |  |
| `fromCache` | `boolean` |  |

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
