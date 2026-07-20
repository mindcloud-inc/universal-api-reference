# Delete Conversation State with Voiceflow

Deletes a user's conversation state from Voiceflow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/state/user/:userId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Delete Conversation State](https://docs.voiceflow.com/api-reference/state/delete-conversation-state)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | ID of the user whose conversation state should be deleted. |
