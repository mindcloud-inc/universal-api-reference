# List Dispatches with Chatvolt AI

Retrieves dispatches from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/dispatches`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List Dispatches](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `number` | no | Number of records to skip for pagination. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `search` | query | `string` | no | Search term for dispatch name. |
| `status` | query | `string` | no | Filter by dispatch status. |
| `agentId` | query | `string` | no | Filter by Agent ID. |
| `crmScenarioId` | query | `string` | no | Filter by CRM Scenario ID. |
| `crmStepId` | query | `string` | no | Filter by CRM Step ID. |
| `startDate` | query | `string` | no | Filter dispatches scheduled on or after this date. |
| `endDate` | query | `string` | no | Filter dispatches scheduled on or before this date. |
| `archived` | query | `boolean` | no | Filter by archived status. |
