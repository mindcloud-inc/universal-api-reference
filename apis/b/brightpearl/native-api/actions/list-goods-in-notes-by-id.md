# List Goods-In Notes by ID with Brightpearl

## Endpoint

- **Method:** `GET`
- **Path:** `/warehouse-service/order/:orderIds/goods-note/goods-in/:goodsInNoteIds`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [List Goods-In Notes by ID](https://api-docs.brightpearl.com/warehouse/goods-in-note/get.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderIds` | path | `string` | yes | Order ID set, maximum 200 IDs. Use * only when supplying specific goods-in note IDs. |
| `goodsInNoteIds` | path | `string` | no | Optional goods-in note ID set, maximum 200 IDs. Required when Order IDs is *. |
