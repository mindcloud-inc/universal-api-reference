# Update Sales Order with Katana

Updates an existing sales order in Katana.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sales_orders/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Sales Order](https://developer.katanamrp.com/reference/update-sales-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Sales order id |
| `order_no` | body | `string` | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `customer_id` | body | `number` | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `order_created_date` | body | `string` | no | — |
| `delivery_date` | body | `string` | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `picked_date` | body | `string` | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `location_id` | body | `number` | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `status` | body | `string` | no | When the status is omitted, NOT_SHIPPED is used as default.         Use PENDING when you want to create sales order quotes. |
| `currency` | body | `string` | no | E.g. USD, EUR. All currently active currency codes in ISO 4217 format.         Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `conversion_rate` | body | `number` | no | Updatable only when sales order status is PACKED or DELIVERED, otherwise it will fail with 422. |
| `conversion_date` | body | `string` | no | Updatable only when sales order status is PACKED or DELIVERED, otherwise it will fail with 422. |
| `additional_info` | body | `string` | no | — |
| `customer_ref` | body | `string` | no | Maximum length: 255. |
| `tracking_number` | body | `string` | no | Maximum length: 256. |
| `tracking_number_url` | body | `string` | no | Maximum length: 2048. |
