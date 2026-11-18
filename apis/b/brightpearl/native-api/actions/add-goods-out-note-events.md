# Add Goods-Out Note Events with Brightpearl

## Endpoint

- **Method:** `POST`
- **Path:** `/warehouse-service/goods-note/goods-out/:goodsOutNoteId/event`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [Add Goods-Out Note Events](https://api-docs.brightpearl.com/warehouse/goods-out-note%20event/post.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goodsOutNoteId` | path | `number` | yes | — |
| `lastEventVersion` | body | `string` | no | Use lastEventVersion from Goods-Out Note GET to prevent duplicate events. |
| `events[]` | body | `array<object>` | yes | — |
| `events[].eventCode` | body | `list<string>` | yes | Accepted values: `PAC`, `PIC`, `PRI`, `SHW`, `UPA`, `UPI`, `UPR`. |
| `events[].occured` | body | `date` | yes | Brightpearl spells this request field occured. |
| `events[].eventOwnerId` | body | `number` | yes | — |
