# Retrieve Lead Purchases with LeadDyno

Retrieves purchases for a specific lead in LeadDyno.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/:id/purchases`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Retrieve Lead Purchases](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/retrieve-purchases-for-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The lead ID. |
| `include_line_items` | query | `boolean` | no | Include detailed line items in the response. |
