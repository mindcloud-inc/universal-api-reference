# List Conversation Participants with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/participants`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [List Conversation Participants](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/list-participants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID whose participants should be listed. |
