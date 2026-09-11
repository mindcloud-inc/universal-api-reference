# Create Product Variant Option with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/catalog/products/:productId/options`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | no | — |
| `type` | body | `string<string>` | yes | BigCommerce API, which determines how it will display on the storefront. Acceptable values: date, checkbox, file, text, multi_line_text, numbers_only_text, radio_buttons, rectangles, dropdown, product_list, product_list_with_images, swatch. Required in a /POST.  Allowed: date \| checkbox \| file \| text \| multi_line_text \| numbers_only_text \| radio_buttons \| rectangles \| dropdown \| product_list \| product_list_with_images \| swatch |
| `display_name` | body | `string` | yes | — |
| `option_values[]` | body | `array` | yes | — |
