# List Agent Tools with Letta

Retrieves tools attached to an agent in Letta.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agent_id/tools`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [List Agent Tools](https://docs.letta.com/api/resources/agents/subresources/tools/methods/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The Letta agent ID. |
