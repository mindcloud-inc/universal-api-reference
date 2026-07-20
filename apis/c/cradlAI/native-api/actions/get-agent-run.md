# Get Agent Run with Cradl AI

Retrieves an agent run from Cradl AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/:agentId/runs/:runId`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Get Agent Run](https://docs.cradl.ai/api-reference/get-agents-runs-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | Identifier of the agent. |
| `runId` | path | `string` | yes | Identifier of the run. |
