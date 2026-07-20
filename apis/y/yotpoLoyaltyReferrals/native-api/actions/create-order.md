# Create Order with Yotpo Loyalty & Referrals

Creates an order in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orders`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Create Order](https://loyaltyapi.yotpo.com/reference/create-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_email` | body | `string` | yes | The customer's email address. |
| `total_amount_cents` | body | `number` | yes | The order total in cents. |
| `currency_code` | body | `string` | yes | The ISO currency code for the order. |
| `order_id` | body | `string` | yes | The merchant order identifier. |
| `ip_address` | body | `string` | yes | The customer's IP address. |
| `user_agent` | body | `string` | yes | The customer's browser or device user agent. |
| `customer_id` | body | `string` | no | The identifier used to uniquely identify the customer in your system. |
| `status` | body | `string` | no | Order status used to determine how Yotpo should process rewards and discount removal. |
| `created_at` | body | `string` | no | Timestamp describing when this order was placed. |
| `coupon_code` | body | `string` | no | Comma-separated list of coupon codes used on the order. |
| `ignore_ip_ua` | body | `boolean` | no | Ignore IP address and user-agent fraud checks for this order. |
| `discount_amount_cents` | body | `number` | no | Total discount amount applied to the order in cents. |
| `tags` | body | `string` | no | Comma-separated list of order tags. |
| `clerk_employee_id` | body | `string` | no | Employee ID of the store clerk who processed the transaction. |
| `clerk_name` | body | `string` | no | Name of the store clerk who processed the transaction. |
| `store_address` | body | `string` | no | Street address of the store location for the order. |
| `store_city` | body | `string` | no | City of the store location for the order. |
| `store_state` | body | `string` | no | State or province of the store location for the order. |
| `channel_type` | body | `string` | no | Order channel, such as online or offline. |
| `items[].id` | body | `string` | no | Unique identifier of a purchased product line item. |
| `items[].name` | body | `string` | no | Customer-facing product name for a purchased item. |
| `items[].quantity` | body | `number` | no | Quantity purchased for the item. |
| `items[].price_cents` | body | `number` | no | Unit price for the item in cents. |
| `items[].collections` | body | `string` | no | Comma-separated collections or tags for the item. |
| `items[].type` | body | `string` | no | Product category or type for the purchased item. |
| `items[].vendor` | body | `string` | no | Vendor or manufacturer for the purchased item. |
| `customer.tags` | body | `string` | no | Comma-separated customer tags. Include this if customer-based include or exclude rules are configured. |
| `customer.has_account` | body | `boolean` | no | Whether the customer has an account with the ecommerce platform. |
| `customer.opted_in` | body | `boolean` | no | Whether the customer should be opted in to the loyalty program. |
| `customer.opted_in_at` | body | `string` | no | Timestamp when the customer opted in to the loyalty program. |
