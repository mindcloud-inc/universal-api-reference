# Update Order with SmartRoutes

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/:id`
- **Base URL:** `https://api.smartroutes.io/v2`
- **Official documentation:** [Update Order](https://api.smartroutes.io/v2/docs/api/#tag/Orders/paths/~1orders~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the order to update. |
| `order_number` | body | `string` | no | Order number. |
| `priority` | body | `string` | no | Priority of the order. |
| `type` | body | `string` | no | Type of the order. Accepted values: `0`, `1`, `2`. |
| `delivery_address` | body | `string` | no | Delivery address. |
| `delivery_country_code` | body | `string` | no | Two letter country code for the delivery address. |
| `delivery_lat` | body | `number` | no | Latitude of the delivery location. |
| `delivery_lng` | body | `number` | no | Longitude of the delivery location. |
| `delivery_duration` | body | `number` | no | Duration for order delivery in minutes. |
| `delivery_date` | body | `string` | no | Date for order delivery in YYYY-MM-DD format. |
| `delivery_notes` | body | `string` | no | Notes for delivery instructions. |
