# List Conversation Messages with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/messages`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [List Conversation Messages](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/list-conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID whose messages you want to list. |
