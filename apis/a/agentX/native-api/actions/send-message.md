# Send Message with AgentX

Sends a message to a conversation in AgentX.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:id/message`
- **Base URL:** `https://api.agentx.so/api/v1/access`
- **Official documentation:** [Send Message](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-message-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation Id |
| `agentMode` | body | `list<string>` | no | Agent mode, can be "chat" or "search" Accepted values: `chat`, `search`. |
| `message` | body | `string` | no | Message to send |
| `context` | body | `number` | no | Memory context amount. 0 means as much as possible, 1 means only the last message, etc. |
