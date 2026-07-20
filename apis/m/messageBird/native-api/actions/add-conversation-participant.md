# Add Conversation Participant with MessageBird

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/participants`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Add Conversation Participant](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/add-participant-to-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID that should receive the participant. |
