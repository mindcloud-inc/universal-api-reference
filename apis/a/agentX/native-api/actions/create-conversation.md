# Create Conversation with AgentX

Creates a new conversation in AgentX.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/:id/conversations/new`
- **Base URL:** `https://api.agentx.so/api/v1/access`
- **Official documentation:** [Create Conversation](https://docs.agentx.so/reference/post_api-v1-access-agents-id-conversations-new-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Agent Id |
| `type` | body | `list<string>` | no | chat, search, ecommerce Accepted values: `chat`, `ecommerce`, `search`. |
