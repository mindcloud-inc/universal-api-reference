# Create Agent Run with Cradl AI

Creates a new agent run in Cradl AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/:agentId/runs`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Create Agent Run](https://docs.cradl.ai/api-reference/post-agents-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | Identifier of the agent that owns the run. |
| `variables` | body | `object` | no | Variables passed to the agent run. |
