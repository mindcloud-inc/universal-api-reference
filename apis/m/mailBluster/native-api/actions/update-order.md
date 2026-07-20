# Update Order with MailBluster

Updates an existing order in MailBluster.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/:orderId`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Update Order](https://app.mailbluster.com/api-doc/orders/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Unique order ID to update. |
| `customer` | body | `object` | no | Updated customer object for the order. |
| `currency` | body | `string` | no | Updated order currency code. |
| `totalPrice` | body | `number` | no | Updated total price of the order. |
| `items[]` | body | `array<object>` | no | Updated array of products included in the order. |
| `campaignId` | body | `number` | no | Updated optional campaign ID to associate with the order. |
