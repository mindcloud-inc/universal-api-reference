# Create Order with Open Letter Connect

Creates an order in Open Letter Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.openletterconnect.com/api/v1`
- **Official documentation:** [Create Order](https://api-docs.openletterconnect.com/orders/place-order/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliveryDate` | body | `string` | yes | The requested delivery date string. |
| `name` | body | `string` | no | An optional name for the order. |
| `productId` | body | `number` | yes | The product ID to order. |
| `tag` | body | `string` | no | The contact tag ID to use as the recipient source for the order. |
| `templateId` | body | `number` | yes | The template ID to use for the order. |
