# Post Payment Batch with Viewpoint Vista

Validate and post an AR Batch

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ar/2/data/batches/actions/post_receipt`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Post Payment Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `__key` | body | `object` | no |
| `PostedDate` | body | `string` | no |
