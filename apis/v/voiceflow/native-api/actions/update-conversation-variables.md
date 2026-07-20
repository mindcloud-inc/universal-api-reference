# Update Conversation Variables with Voiceflow

Updates a user's conversation variables in Voiceflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/state/user/:userId/variables`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Update Conversation Variables](https://docs.voiceflow.com/api-reference/state/update-conversation-variables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | ID of the user whose conversation variables should be merged. |
| `variables` | body | `object` | yes | Object of variable keys and values to merge into the user state. |
