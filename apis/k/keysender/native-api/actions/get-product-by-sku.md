# Get Product By SKU with Keysender

Retrieves a product from Keysender by SKU.

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog/products/:sku`
- **Base URL:** `https://panel.keysender.co.uk/api/v1.0`
- **Official documentation:** [Get Product By SKU](https://panel.keysender.co.uk/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | path | `string` | yes | The product SKU. |
| `additional_information` | query | `boolean` | no | Include expanded product information when true. |
