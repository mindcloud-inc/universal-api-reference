# Retrieve Agent Memory Block with Letta

Retrieves a core memory block from Letta by label.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agent_id/core-memory/blocks/:block_label`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Retrieve Agent Memory Block](https://docs.letta.com/api/resources/agents/subresources/blocks/methods/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
| `block_label` | path | `string` | yes | The label of the memory block attached to the agent. |
