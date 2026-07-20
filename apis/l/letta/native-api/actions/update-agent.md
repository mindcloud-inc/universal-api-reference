# Update Agent with Letta

Updates an existing agent in Letta.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/agents/:agent_id`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Update Agent](https://docs.letta.com/api/resources/agents/methods/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
| `name` | body | `string` | no | Optional updated display name for the agent. |
