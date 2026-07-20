# Retrieve Purchase By Code with LeadDyno

Retrieves a purchase from LeadDyno by purchase code.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchases/by_purchase_code`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Retrieve Purchase By Code](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/get-purchases-by-purchase-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_line_items` | query | `boolean` | no | Include detailed line items in the response. |
| `purchase_code` | query | `string` | yes | A unique identifier associated with the purchase to retrieve. |
