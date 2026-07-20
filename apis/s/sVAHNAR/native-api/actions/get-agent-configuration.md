# Get Agent Configuration with SVAHNAR

Retrieves an agent configuration from SVAHNAR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/download-agent/:agent_id`
- **Base URL:** `https://api.svahnar.com`
- **Official documentation:** [Get Agent Configuration](https://docs.svahnar.com/docs/Agents/get_agent_details/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The unique identifier of the agent. |
