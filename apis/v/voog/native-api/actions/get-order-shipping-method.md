# Get Order Shipping Method with Voog

Retrieves the shipping method for a Voog order.

## Endpoint

- **Method:** `GET`
- **Path:** `/ecommerce/v1/orders/:orderId/shipping_method`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Get Order Shipping Method](https://www.voog.com/developers/api/ecommerce/orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Numeric order ID. |
