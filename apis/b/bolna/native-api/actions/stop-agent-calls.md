# Stop Agent Calls with Bolna

Stops queued calls for a specific Bolna agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/agent/:agentId/stop`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [Stop Agent Calls](https://www.bolna.ai/docs/api-reference/agent/v2/stop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The ID of the agent. |
