# Request Shipping Label with Stockpilot

Requests a shipping label in Stockpilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipping/request-label`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Request Shipping Label](https://api.stockpilot.dev/redoc#operation/request_label_shipping_request_label_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | body | `string` | yes |
| `carrier_id` | body | `string` | yes |
| `order_pk` | body | `number` | yes |
