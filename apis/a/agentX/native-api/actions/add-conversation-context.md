# Add Conversation Context with AgentX

Updates conversation context in AgentX without triggering chat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/:id/update-context`
- **Base URL:** `https://api.agentx.so/api/v1/access`
- **Official documentation:** [Add Conversation Context](https://docs.agentx.so/reference/put_api-v1-access-conversations-id-update-context-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation Id |
| `messages[]` | body | `array<object>` | no | Array of conversation context messages shaped as {"user":"..."} or {"assistant":"..."} |
