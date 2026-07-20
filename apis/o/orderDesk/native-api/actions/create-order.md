# Create Order with Order Desk

Creates a new order in Order Desk.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Create Order](https://apidocs.orderdesk.com/?shell=#create-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Customer email address. |
| `shipping_method` | body | `string` | no | Shipping method label. |
| `shipping.first_name` | body | `string` | yes | Shipping first name. |
| `shipping.last_name` | body | `string` | yes | Shipping last name. |
| `shipping.address1` | body | `string` | yes | Shipping street address. |
| `shipping.city` | body | `string` | yes | Shipping city. |
| `shipping.state` | body | `string` | yes | Shipping state or region. |
| `shipping.postal_code` | body | `string` | yes | Shipping postal code. |
| `shipping.country` | body | `string` | yes | Shipping country code or full country name. |
| `customer.first_name` | body | `string` | yes | Customer first name. |
| `customer.last_name` | body | `string` | yes | Customer last name. |
| `customer.address1` | body | `string` | yes | Customer street address. |
| `customer.city` | body | `string` | yes | Customer city. |
| `customer.state` | body | `string` | yes | Customer state or region. |
| `customer.postal_code` | body | `string` | yes | Customer postal code. |
| `customer.country` | body | `string` | yes | Customer country code or full country name. |
| `order_items[].name` | body | `string` | yes | Order item name. |
| `order_items[].price` | body | `number` | yes | Order item unit price. |
| `order_items[].quantity` | body | `number` | yes | Order item quantity. |
| `order_items[].code` | body | `string` | yes | Order item SKU or code. |
