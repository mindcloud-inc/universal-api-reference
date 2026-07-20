# Update Product with Goodbarber eCommerce

## Endpoint

- **Method:** `PATCH`
- **Path:** `/publicapi/v2/general/catalog/:webzine_id/product/:product_id/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [Update Product](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | Product ID. |
| `title` | body | `string` | no | Product title. |
| `summary` | body | `string` | no | Short product summary. |
| `status` | body | `string` | no | Product publication status. |
