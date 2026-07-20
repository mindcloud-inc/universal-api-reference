# List Participant Conversations with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/participants/:conversationParticipantId/conversations`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [List Participant Conversations](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/list-participant-conversations-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the participant. |
| `conversationParticipantId` | path | `string` | yes | The Bird conversation participant ID whose conversations should be listed. |
