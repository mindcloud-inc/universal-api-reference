# Retrieve Shipping Label with Stockpilot

Retrieves a shipping label from Stockpilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipping/retrieve-label`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Retrieve Shipping Label](https://api.stockpilot.dev/redoc#operation/retrieve_label_shipping_retrieve_label_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_id` | body | `string` | yes |
| `service` | body | `string` | yes |
| `order_pk` | body | `number` | yes |
