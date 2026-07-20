# Create Agent with Letta

Creates a new agent in Letta.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Create Agent](https://docs.letta.com/api/resources/agents/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | Model handle to use for the new Letta agent, such as openai/gpt-4.1. |
| `name` | body | `string` | no | Optional display name for the agent. |
| `block_ids[]` | body | `array<string>` | no | Optional Letta block IDs to attach to the agent when it is created. |
| `memory_blocks[]` | body | `array<object>` | no | Optional memory blocks to create in the agent's in-context memory. |
