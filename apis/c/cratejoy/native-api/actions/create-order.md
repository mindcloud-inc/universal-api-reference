# Create Order with Cratejoy

Creates a new order in Cratejoy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/orders/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Create Order](https://docs.cratejoy.com/reference/order-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer.id` | body | `number` | yes | The existing Cratejoy customer ID for the order. |
| `ship_address_id` | body | `number` | no | The shipping address ID to use for the order. |
| `cust_pay_id` | body | `number` | no | The customer's saved payment method ID for the order. |
| `coupons` | body | `string` | no | Coupon codes to apply to the order. |
| `products[].product_instance.id` | body | `number` | yes | The product instance ID for an order line item. |
| `products[].term.num_cycles` | body | `number` | no | The number of prepaid cycles for a subscription product term. |
| `products[].quantity` | body | `number` | no | The quantity for an order line item. |
| `order_gift_info.gift_message` | body | `string` | no | The gift message for the order gift info. |
