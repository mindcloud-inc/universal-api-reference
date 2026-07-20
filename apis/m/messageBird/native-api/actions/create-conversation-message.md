# Create Conversation Message with MessageBird

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/messages`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Create Conversation Message](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/create-conversation-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID where you want to create the message. |
