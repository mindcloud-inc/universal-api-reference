# Update Agent Run with Cradl AI

Updates an existing agent run in Cradl AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agents/:agentId/runs/:runId`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Update Agent Run](https://docs.cradl.ai/api-reference/patch-agents-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | Identifier of the agent that owns the run. |
| `runId` | path | `string` | yes | Identifier of the run to update. |
| `status` | body | `string` | no | Updated status for the run. |
