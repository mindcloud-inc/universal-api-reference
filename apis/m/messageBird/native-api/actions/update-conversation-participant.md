# Update Conversation Participant with MessageBird

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/participants/:conversationParticipantId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Update Conversation Participant](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/update-participant-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID that owns the participant. |
| `conversationParticipantId` | path | `string` | yes | The Bird conversation participant ID to update. |
