# Create Agent Message with Letta

Processes a user message through an agent in Letta.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/:agent_id/messages`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Create Agent Message](https://docs.letta.com/api/resources/agents/subresources/messages/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
| `input` | body | `string` | yes | The user message to send to the agent. |
