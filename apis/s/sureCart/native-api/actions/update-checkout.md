# Update Checkout with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/checkouts/:id`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Update Checkout](https://developer.surecart.com/api-reference/checkouts/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The checkout ID to update. |
| `checkout.line_items[].price_id` | body | `string` | yes | The price ID for a checkout line item. |
| `checkout.line_items[].quantity` | body | `number` | yes | The quantity for a checkout line item. |
