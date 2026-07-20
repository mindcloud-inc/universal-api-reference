# Create Order with Envoice

Creates a new order in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `order/new`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Create Order](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CurrencyId` | body | `number` | yes | Currency identifier. |
| `Items` | body | `string` | yes | JSON array of order item objects. |
| `Name` | body | `string` | yes | Order name. |
| `OrderBillingDetails` | body | `string` | no | JSON object with order billing details. |
| `OrderShippingDetails` | body | `string` | no | JSON object with order shipping details. |
| `ProductId` | body | `number` | no | Product identifier for the order. |
| `ShippingAmount` | body | `number` | no | Order shipping amount. |
| `Status` | body | `string` | yes | Order status. |
| `SubTotalAmount` | body | `number` | no | Order subtotal amount. |
| `TaxAmount` | body | `number` | no | Order tax amount. |
| `TotalAmount` | body | `number` | yes | Order total amount. |
