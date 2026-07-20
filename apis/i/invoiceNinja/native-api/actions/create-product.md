# Create Product with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Create Product](https://api-docs.invoicing.co/#tag/products/operation/storeProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_key` | body | `string` | yes | Invoice Ninja product key. |
| `notes` | body | `string` | no | Notes or description for the product. |
| `cost` | body | `number` | yes | Product cost. |
| `price` | body | `number` | yes | Product price. |
| `quantity` | body | `number` | no | Product quantity. The docs show a default of 1. |
