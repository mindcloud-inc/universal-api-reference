# Update Conversation Message with MessageBird

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/messages/:messageId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Update Conversation Message](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/update-conversation-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID that owns the message. |
| `messageId` | path | `string` | yes | The Bird message ID to update. |
