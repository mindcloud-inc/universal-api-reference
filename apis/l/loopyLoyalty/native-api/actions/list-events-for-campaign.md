# List Events For Campaign with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/events/analytics/transactions/:cid`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [List Events For Campaign](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_listEventsForCampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | yes | Campaign ID. |
| `dt.start` | body | `string` | no | Initial paging row start number, 0 based. |
| `dt.length` | body | `string` | no | Number of rows to return. |
| `dt.search` | body | `string` | no | Search term applied to username. |
| `dt.order.column` | body | `string` | no | Column to sort by. |
| `dt.order.dir` | body | `string` | no | Sort direction. |
| `count` | body | `boolean` | no | Indicates if a count is returned or a list of records. |
