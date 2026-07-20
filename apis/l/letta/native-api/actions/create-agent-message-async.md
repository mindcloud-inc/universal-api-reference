# Create Agent Message Async with Letta

Starts an asynchronous agent message run in Letta.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/:agent_id/messages/async`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Create Agent Message Async](https://docs.letta.com/api/resources/agents/subresources/messages/methods/create-async)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
| `input` | body | `string` | yes | The user message to send to the agent asynchronously. |
