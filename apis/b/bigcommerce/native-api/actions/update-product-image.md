# Update Product Image with BigCommerce

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/catalog/products/:productId/images/:imageId`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The product type. One of: physical - a physical stock unit, digital - a digital download. |
| `image_url` | body | `string` | yes | A unique product name. |
| `sort_order` | body | `number` | no | Weight of the product, which can be used when calculating shipping costs. This is based on the unit set on the store |
| `is_thumbnail` | body | `boolean` | no | Flag to determine whether the product should be displayed to customers browsing the store. If true, the product will be displayed. If false, the product will be hidden from view Format: `text`. |
| `productId` | path | `string` | no | — |
| `imageId` | path | `string` | no | — |
