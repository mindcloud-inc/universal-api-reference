# Create CRM Scenario with Chatvolt AI

Creates a new CRM scenario in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/scenario`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create CRM Scenario](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/create-scenario)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name for the new CRM scenario. |
| `description` | body | `string` | no | An optional description for the CRM scenario. |
