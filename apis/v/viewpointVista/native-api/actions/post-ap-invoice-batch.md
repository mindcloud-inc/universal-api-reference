# Post AP Invoice Batch with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ap/2/data/inv_batches/actions/post`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Post AP Invoice Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaap2datainv_batchesactionspost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista AP company code. |
| `Mth` | body | `string` | yes | Vista AP batch month in YYYY-MM-01 format. |
| `BatchId` | body | `number` | yes | Vista AP invoice batch identifier to post. |
