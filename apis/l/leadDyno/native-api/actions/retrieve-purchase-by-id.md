# Retrieve Purchase By ID with LeadDyno

Retrieves a purchase from LeadDyno by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchases/:id`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Retrieve Purchase By ID](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/get-purchases-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The purchase ID. |
| `include_line_items` | query | `boolean` | no | Include detailed line items in the response. |
