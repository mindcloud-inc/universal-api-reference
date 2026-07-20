# Update Product with Envoice

Updates an existing product in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `product/update`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Update Product](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CurrencyId` | body | `number` | yes | Currency identifier. |
| `Description` | body | `string` | no | Product description. |
| `Id` | body | `number` | yes | Product identifier. |
| `Items` | body | `string` | yes | JSON array of product item objects. |
| `Name` | body | `string` | yes | Product name. |
| `PaymentGateways` | body | `string` | no | JSON array of product payment gateway objects. |
| `Status` | body | `string` | yes | Product availability status. |
