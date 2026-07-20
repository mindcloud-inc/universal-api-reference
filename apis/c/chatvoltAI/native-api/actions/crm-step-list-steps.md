# List CRM Steps with Chatvolt AI

Retrieves CRM steps from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/crm/step`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List CRM Steps](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/list-steps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | query | `string` | yes | The ID of the CRM scenario to fetch steps for. |
| `agentId` | query | `string` | no | Filter steps by a specific Agent ID. |
