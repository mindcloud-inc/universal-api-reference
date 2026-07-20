# Create Purchase with LeadDyno

Creates a new purchase in LeadDyno.

## Endpoint

- **Method:** `POST`
- **Path:** `/purchases`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Create Purchase](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/post-purchases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | no | The affiliate code to which the purchase should be assigned. |
| `currency` | body | `string` | no | The purchase currency. |
| `email` | body | `string` | yes | The email address of the customer who made the purchase. |
| `purchase_code` | body | `string` | no | A unique identifier for this purchase. |
| `purchase_amount` | body | `number` | no | The total amount of the purchase. |
