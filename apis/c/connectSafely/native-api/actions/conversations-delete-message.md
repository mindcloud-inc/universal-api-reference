# Delete (recall) a message with ConnectSafely

Recall a message you sent. The message is first recalled on LinkedIn (source of truth); only on success is it soft-deleted locally so a later sync never re-surfaces the recalled tombstone. Other connected clients/tabs are notified via WebSocket. Matching is by the prefix-independent normalized message id, so the stored row is removed even if it was synced under a different mailbox prefix.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/conversations/:conversationUrn/messages/:messageUrn`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Delete (recall) a message](https://connectsafely.ai/docs/api/linkedin-messaging/delete-conversations-conversationurn-messages-messageurn-conversations-delete-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationUrn` | param | `string` | yes | Conversation URN (URL-encoded) |
| `messageUrn` | param | `string` | yes | URN of the message to delete (URL-encoded) |
| `accountId` | query | `string` | no | LinkedIn account ID |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `messageUrn` | `string` |  |

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
