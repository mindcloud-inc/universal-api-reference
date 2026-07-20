# Update Order with Voog

Updates an existing order in the current Voog store.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ecommerce/v1/orders/:orderId`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Update Order](https://www.voog.com/developers/api/ecommerce/orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note` | body | `string` | no | Internal note for the order. |
| `orderId` | path | `number` | yes | Numeric order ID. |
| `payment_status` | body | `string` | no | Order payment status. |
| `shipping_status` | body | `string` | no | Order shipping status. |
| `status` | body | `string` | no | Order general status. |
