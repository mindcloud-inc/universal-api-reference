# List Agent Memory Blocks with Letta

Retrieves core memory blocks for an agent in Letta.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agent_id/core-memory/blocks`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [List Agent Memory Blocks](https://docs.letta.com/api/resources/agents/subresources/blocks/methods/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
