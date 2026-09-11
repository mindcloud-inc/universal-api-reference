# Update Product with BigCommerce

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/catalog/products/:productId`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A unique product name. |
| `productId` | path | `string` | yes | — |
| `type` | body | `string` | yes | The product type. One of: physical - a physical stock unit, digital - a digital download. |
| `sku` | body | `string` | no | A unique user-defined alphanumeric product code/stock keeping unit (SKU) |
| `weight` | body | `number` | no | Weight of the product, which can be used when calculating shipping costs. This is based on the unit set on the store |
| `price` | body | `number` | no | The price of the product. The price should include or exclude tax, based on the store settings |
| `is_visible` | body | `boolean` | no | Flag to determine whether the product should be displayed to customers browsing the store. If true, the product will be displayed. If false, the product will be hidden from view Format: `toggle`. |
| `inventory_level` | body | `number` | no | The amount in inventory |
