# Send Message SSE with AgentX

Sends a conversation message over SSE in AgentX.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:id/messagesse`
- **Base URL:** `https://api.agentx.so/api/v1/access`
- **Official documentation:** [Send Message SSE](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-messagesse-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation Id |
| `message` | body | `string` | yes | Message to send |
| `context` | body | `number` | no | Context for the message |
