# Delete Agent with SVAHNAR

Deletes an existing agent from SVAHNAR.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/agents/delete`
- **Base URL:** `https://api.svahnar.com`
- **Official documentation:** [Delete Agent](https://docs.svahnar.com/docs/Agents/delete_agent/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | yes | The unique identifier of the agent to delete. |
