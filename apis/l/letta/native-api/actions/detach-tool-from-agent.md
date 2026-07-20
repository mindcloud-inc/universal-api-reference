# Detach Tool From Agent with Letta

Detaches a tool from an agent in Letta.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/agents/:agent_id/tools/detach/:tool_id`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Detach Tool From Agent](https://docs.letta.com/api/resources/agents/subresources/tools/methods/detach)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
| `tool_id` | path | `string` | yes | The Letta tool ID to detach. |
