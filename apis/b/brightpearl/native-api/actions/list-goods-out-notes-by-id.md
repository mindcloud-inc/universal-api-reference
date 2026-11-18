# List Goods-Out Notes by ID with Brightpearl

## Endpoint

- **Method:** `GET`
- **Path:** `/warehouse-service/order/:orderIds/goods-note/goods-out/:goodsOutNoteIds`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [List Goods-Out Notes by ID](https://api-docs.brightpearl.com/warehouse/goods-out-note/get.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderIds` | path | `string` | yes | Order ID set, maximum 500 IDs. Use * only when supplying specific goods-out note IDs. |
| `goodsOutNoteIds` | path | `string` | no | Optional goods-out note ID set, maximum 500 IDs. Required when Order IDs is *. |
