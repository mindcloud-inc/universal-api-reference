# Create Product with Envoice

Creates a new product in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `product/new`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Create Product](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ButtonCallToAction` | body | `string` | no | Product checkout button call to action. |
| `CurrencyId` | body | `number` | yes | Currency identifier. |
| `Description` | body | `string` | no | Product description. |
| `IsFeatured` | body | `boolean` | no | Whether the product is featured. |
| `Items` | body | `string` | yes | JSON array of product item objects. |
| `Name` | body | `string` | yes | Product name. |
| `PaymentGateways` | body | `string` | no | JSON array of product payment gateway objects. |
| `ShippingAmount` | body | `number` | no | Product shipping amount. |
| `ShippingDescription` | body | `string` | no | Shipping description. |
| `Status` | body | `string` | yes | Product availability status. |
