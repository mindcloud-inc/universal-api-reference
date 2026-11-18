# Create Goods-In Note with Brightpearl

## Endpoint

- **Method:** `POST`
- **Path:** `/warehouse-service/order/:orderId/goods-note/goods-in`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [Create Goods-In Note](https://api-docs.brightpearl.com/warehouse/goods-in-note/post.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | — |
| `warehouseId` | body | `number` | no | — |
| `goodsMoved[]` | body | `array<object>` | no | — |
| `goodsMoved[].productId` | body | `number` | no | — |
| `goodsMoved[].purchaseOrderRowId` | body | `number` | no | — |
| `goodsMoved[].quantity` | body | `number` | no | — |
| `goodsMoved[].destinationLocationId` | body | `number` | no | — |
| `goodsMoved[].productValue` | body | `object` | no | — |
| `goodsMoved[].productValue.currency` | body | `string` | no | — |
| `goodsMoved[].productValue.value` | body | `number` | no | — |
| `transfer` | body | `boolean` | no | — |
| `receivedOn` | body | `date` | no | — |
| `userBatchReference` | body | `string` | no | Optional reference that must be unique across goods-in notes. |
