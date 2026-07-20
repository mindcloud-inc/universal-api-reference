# List Orders with SmartRoutes

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.smartroutes.io/v2`
- **Official documentation:** [List Orders](https://api.smartroutes.io/v2/docs/api/#tag/Orders/paths/~1orders/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter orders by status. |
| `customer_id` | query | `number` | no | Filter orders by customer ID. |
| `order_number` | query | `string` | no | Filter orders by order number. |
| `updated_at_min` | query | `date` | no | Minimum updated date and time for filtering. |
