# Create Goods-Out Notes with Brightpearl

## Endpoint

- **Method:** `POST`
- **Path:** `/warehouse-service/order/:orderId/goods-note/goods-out`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [Create Goods-Out Notes](https://api-docs.brightpearl.com/warehouse/goods-out-note/post.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | — |
| `warehouses[]` | body | `array<object>` | no | — |
| `warehouses[].warehouseId` | body | `number` | no | — |
| `warehouses[].products[]` | body | `array<object>` | no | — |
| `warehouses[].products[].productId` | body | `number` | no | — |
| `warehouses[].products[].salesOrderRowId` | body | `number` | no | — |
| `warehouses[].products[].quantity` | body | `number` | no | — |
| `warehouses[].releaseDate` | body | `date` | no | — |
| `warehouses[].transfer` | body | `boolean` | no | — |
| `priority` | body | `boolean` | no | — |
| `shippingMethodId` | body | `number` | no | — |
| `labelUri` | body | `string` | no | Maximum length: 512. |
