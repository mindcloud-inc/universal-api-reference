# Create Deal For Organization with Agendor

Creates a new deal for an organization in Agendor.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organization_id/deals`
- **Base URL:** `https://api.agendor.com.br/v3`
- **Official documentation:** [Create Deal For Organization](https://api.agendor.com.br/docs/#operation/Create%20deal%20for%20organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal` | body | `string` | yes | Deal payload as a JSON string matching Agendor's create deal for organization body. |
| `organization_id` | path | `number` | yes | ID of the organization that will own the deal. |
