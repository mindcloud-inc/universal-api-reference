# Delete Agent Run with Cradl AI

Deletes an existing agent run from Cradl AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/agents/:agentId/runs/:runId`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Delete Agent Run](https://docs.cradl.ai/api-reference/delete-agents-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | Identifier of the agent that owns the run. |
| `runId` | path | `string` | yes | Identifier of the run to delete. |
