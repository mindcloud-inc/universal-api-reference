# Create Order with SalesDrive

Creates a new order in SalesDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/handler/`
- **Base URL:** `https://{account}.salesdrive.me`
- **Official documentation:** [Create Order](https://api.salesdrive.me/api/docs/#/order/order-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fName` | body | `string` | no | Customer first name. |
| `lName` | body | `string` | no | Customer last name. |
| `phone` | body | `string` | no | Customer phone number. |
| `email` | body | `string` | no | Customer email address. |
| `products[]` | body | `array<object>` | no | Array of products for the order. |
| `payment_method` | body | `string` | no | Payment method. |
| `shipping_method` | body | `string` | no | Shipping method. |
| `shipping_address` | body | `string` | no | Delivery address. |
| `comment` | body | `string` | no | Order comment. |
| `externalId` | body | `string` | no | External order number. |
