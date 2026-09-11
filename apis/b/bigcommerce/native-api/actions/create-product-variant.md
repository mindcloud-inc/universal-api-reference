# Create Product Variant with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/catalog/products/:productId/variants`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `price` | body | `number` | yes | The price of the product. The price should include or exclude tax, based on the store settings |
| `sku` | body | `string` | no | A unique user-defined alphanumeric product code/stock keeping unit (SKU) |
| `option_values[]` | body | `array` | no | Ex:  "option_values": [     {       "option_display_name": "Color",       "label": "Beige",       "id": 146,       "option_id": 151     }   ] |
| `productId` | path | `string` | no | — |
| `inventory_level` | body | `string` | no | — |
