# Update Purchase with LeadDyno

Updates an existing purchase in LeadDyno.

## Endpoint

- **Method:** `PUT`
- **Path:** `/purchases/:id`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Update Purchase](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/update-a-purchase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | no | The purchase currency. |
| `description` | body | `string` | no | A text description of the purchase. |
| `id` | path | `number` | yes | The purchase ID. |
| `purchase_amount` | body | `number` | no | The purchase amount. |
