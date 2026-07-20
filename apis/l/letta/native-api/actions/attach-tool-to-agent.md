# Attach Tool To Agent with Letta

Attaches a tool to an agent in Letta.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/agents/:agent_id/tools/attach/:tool_id`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Attach Tool To Agent](https://docs.letta.com/api/resources/agents/subresources/tools/methods/attach)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
| `tool_id` | path | `string` | yes | The Letta tool ID to attach. |
