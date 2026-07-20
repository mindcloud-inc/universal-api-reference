# Get Conversation State with Voiceflow

Retrieves a user's conversation state from Voiceflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/state/user/:userId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Get Conversation State](https://docs.voiceflow.com/api-reference/state/get-conversation-state)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Unique ID of the user whose conversation state you want to fetch. |
