# Update Product with ConfigCat

Updates an existing product in ConfigCat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/products/:productId`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [Update Product](https://configcat.com/docs/api/reference/update-product/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | The identifier of the Product. |
| `product` | body | `object` | yes | Raw ConfigCat product body. |
