# Update Conversation with MessageBird

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Update Conversation](https://docs.bird.com/api/conversations-api/api-reference/conversations-management/update-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID to update. |
