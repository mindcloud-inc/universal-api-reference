# Create Order with MailBluster

Creates a new order in MailBluster.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Create Order](https://app.mailbluster.com/api-doc/orders/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Unique order ID in MailBluster. |
| `customer` | body | `object` | yes | Customer object for the order, including email and optional name/subscription fields. |
| `currency` | body | `string` | yes | Order currency code, such as USD. |
| `totalPrice` | body | `number` | yes | Total price of the order. |
| `items[]` | body | `array<object>` | yes | Array of products included in the order. |
| `campaignId` | body | `number` | no | Optional campaign ID to associate with the order. |
