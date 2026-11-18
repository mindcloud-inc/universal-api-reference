# Delete Goods-Out Note with Brightpearl

## Endpoint

- **Method:** `DELETE`
- **Path:** `/warehouse-service/order/:orderId/goods-note/goods-out/:goodsOutNoteId`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [Delete Goods-Out Note](https://api-docs.brightpearl.com/warehouse/goods-out-note/delete.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `number` | yes |
| `goodsOutNoteId` | path | `number` | yes |
