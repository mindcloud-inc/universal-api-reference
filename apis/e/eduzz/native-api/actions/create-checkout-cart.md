# Create Checkout Cart with Eduzz

Creates a checkout cart in Eduzz.

## Endpoint

- **Method:** `POST`
- **Path:** `/sun/v1/cart`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [Create Checkout Cart](https://developers.eduzz.com/reference/api/post-sun-v1-cart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer.email` | body | `string` | no | Customer email address. |
| `customer.name` | body | `string` | no | Customer full name. |
| `items[].description` | body | `string` | no | Line item description shown in checkout. |
| `items[].price.currency` | body | `string` | no | Line item currency. |
| `items[].price.value` | body | `string` | no | Line item price value. |
| `items[].productId` | body | `string` | no | Product id to add to the cart. |
| `items[].quantity` | body | `string` | no | Line item quantity. |
| `orderId` | body | `string` | no | Your internal order reference. |
| `postbackUrl` | body | `string` | no | Webhook URL for cart events. |
| `returnUrl` | body | `string` | no | Buyer return URL after checkout. |
