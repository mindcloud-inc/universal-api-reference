# Create Product with Goodbarber eCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/v2/general/catalog/:webzine_id/product/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [Create Product](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Product title. |
| `summary` | body | `string` | no | Short product summary. |
| `status` | body | `string` | no | Product publication status. |
| `slug` | body | `string` | no | Product slug. |
| `show_similar_products` | body | `boolean` | no | Whether related products should be shown. |
| `collections[]` | body | `array<number>` | yes | Collection IDs assigned to the product. |
| `tags[]` | body | `array<string>` | yes | Tags assigned to the product. |
| `set_custom_similar_products[]` | body | `array<number>` | yes | Explicit related product IDs. |
