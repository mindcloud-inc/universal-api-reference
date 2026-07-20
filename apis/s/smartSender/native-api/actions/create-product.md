# Create Product with Smart Sender

Creates a new product in Smart Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/products`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Create Product](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97255432)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | body | `string` | no | Category identifier for the product. |
| `essences[]` | body | `array<object>` | yes | Array of product essence objects without temporary values. |
| `labels[]` | body | `array<string>` | no | Array of label identifiers assigned to the product. |
| `name` | body | `string` | yes | Product name, unique within the project. |
| `paymentSystems[]` | body | `array<string>` | no | Array of payment system identifiers available for the product. |
