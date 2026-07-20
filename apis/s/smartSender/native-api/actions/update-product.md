# Update Product with Smart Sender

Updates an existing product in Smart Sender.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/products/:productId`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Update Product](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97255432)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | body | `string` | no | Updated category identifier for the product. |
| `essences[]` | body | `array<object>` | no | Updated array of product essence objects without temporary values. |
| `labels[]` | body | `array<string>` | no | Updated array of label identifiers assigned to the product. |
| `name` | body | `string` | no | Updated product name, unique within the project. |
| `paymentSystems[]` | body | `array<string>` | no | Updated array of payment system identifiers available for the product. |
| `productId` | path | `string` | yes | The Smart Sender product ID. |
