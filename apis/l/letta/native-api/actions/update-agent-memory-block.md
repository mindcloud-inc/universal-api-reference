# Update Agent Memory Block with Letta

Updates a core memory block in Letta by label.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/agents/:agent_id/core-memory/blocks/:block_label`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Update Agent Memory Block](https://docs.letta.com/api/resources/agents/subresources/blocks/methods/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
| `block_label` | path | `string` | yes | The label of the memory block attached to the agent. |
| `value` | body | `string` | yes | The updated memory block value. |
