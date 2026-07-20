# Update Product with WEBLUCY

Updates an existing product in WEBLUCY.

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/{id}`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [Update Product](https://websitebuilder.docs.apiary.io/#reference/products/single-product/update-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The product ID. |
| `variants[]` | body | `array<object>` | no | The product variants carrying pricing and inventory details. |
