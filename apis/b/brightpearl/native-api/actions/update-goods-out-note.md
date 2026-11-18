# Update Goods-Out Note with Brightpearl

## Endpoint

- **Method:** `PUT`
- **Path:** `/warehouse-service/goods-note/goods-out/:goodsOutNoteId`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [Update Goods-Out Note](https://api-docs.brightpearl.com/warehouse/goods-out-note/put.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goodsOutNoteId` | path | `number` | yes | — |
| `priority` | body | `boolean` | no | — |
| `shipping` | body | `object` | no | — |
| `shipping.shippingMethodId` | body | `number` | no | — |
| `shipping.reference` | body | `string` | no | Maximum length: 64. |
| `shipping.boxes` | body | `number` | no | — |
| `shipping.weight` | body | `string` | no | Total weight, at most 999999.99. |
| `labelUri` | body | `string` | no | Maximum length: 512. |
