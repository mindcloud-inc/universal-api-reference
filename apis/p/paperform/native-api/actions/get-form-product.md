# Get Form Product with Paperform

Retrieves a product from a Paperform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:slug_or_id/products/:product_sku`
- **Base URL:** `https://api.paperform.co/v1`
- **Official documentation:** [Get Form Product](https://paperform.readme.io/reference/getformproduct)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `slug_or_id` | path | `list<string>` | yes |
| `product_sku` | path | `list` | yes |
