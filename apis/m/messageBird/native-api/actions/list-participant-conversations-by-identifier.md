# List Participant Conversations by Identifier with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/participants/:identifierKey/:identifierValue/conversations`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [List Participant Conversations by Identifier](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/list-participant-conversations-by-identifier-key-and-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the participant. |
| `identifierKey` | path | `string` | yes | The participant identifier key, such as emailaddress or phonenumber. |
| `identifierValue` | path | `string` | yes | The participant identifier value to match. |
