# List Agent Runs with Cradl AI

Retrieves all agent runs from Cradl AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/:agentId/runs`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [List Agent Runs](https://docs.cradl.ai/api-reference/get-agents-runs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | Identifier of the agent whose runs to list. |
| `history` | query | `string` | no | History filter for runs. |
| `status` | query | `string` | no | Status filter for runs. |
| `sort` | query | `string` | no | Sort order for runs. |
| `createdTimeAfter` | query | `date` | no | Return runs created after this timestamp. |
| `createdTimeBefore` | query | `date` | no | Return runs created before this timestamp. |
| `updatedTimeAfter` | query | `date` | no | Return runs updated after this timestamp. |
| `updatedTimeBefore` | query | `date` | no | Return runs updated before this timestamp. |
