# Get Conversation Participant by Identifier with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/participants/:identifierKey/:identifierValue`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Get Conversation Participant by Identifier](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/get-participant-by-identifier-key-and-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID that owns the participant. |
| `identifierKey` | path | `string` | yes | The participant identifier key, such as emailaddress or phonenumber. |
| `identifierValue` | path | `string` | yes | The participant identifier value to match. |
