# Delete Conversation Message with MessageBird

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/messages/:messageId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Delete Conversation Message](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/delete-conversation-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID that owns the message. |
| `messageId` | path | `string` | yes | The Bird message ID to delete. |
