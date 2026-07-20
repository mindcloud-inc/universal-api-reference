# Update CRM Scenario with Chatvolt AI

Updates an existing CRM scenario in Chatvolt AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/scenario`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update CRM Scenario](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/update-scenario)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the CRM scenario to update. |
| `name` | body | `string` | yes | The new name for the CRM scenario. |
| `description` | body | `string` | no | An optional new description for the CRM scenario. |
