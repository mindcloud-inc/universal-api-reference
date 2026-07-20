# Delete Conversation with MessageBird

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Delete Conversation](https://docs.bird.com/api/conversations-api/api-reference/conversations-management/delete-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID you want to delete. |
