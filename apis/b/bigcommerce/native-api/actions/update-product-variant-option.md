# Update Product Variant Option with BigCommerce

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/catalog/products/:productId/options/:optionId`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | — |
| `type` | body | `string<string>` | yes | BigCommerce API, which determines how it will display on the storefront. Acceptable values: date, checkbox, file, text, multi_line_text, numbers_only_text, radio_buttons, rectangles, dropdown, product_list, product_list_with_images, swatch. Required in a /POST.  Allowed: date \| checkbox \| file \| text \| multi_line_text \| numbers_only_text \| radio_buttons \| rectangles \| dropdown \| product_list \| product_list_with_images \| swatch |
| `display_name` | body | `string` | no | — |
| `option_values[]` | body | `array` | no | — |
| `optionId` | path | `string` | yes | — |
