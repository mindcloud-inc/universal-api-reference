# Update Conversation State with Voiceflow

Updates a user's conversation state in Voiceflow.

## Endpoint

- **Method:** `PUT`
- **Path:** `/state/user/:userId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Update Conversation State](https://docs.voiceflow.com/api-reference/state/update-conversation-state)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | ID of the user whose conversation state should be replaced. |
| `state` | body | `object` | yes | Full conversation state object with stack, variables, storage, and turn. |
