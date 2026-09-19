# Post Change Order Batch with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/po/2/data/co_batches/actions/post`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Post Change Order Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapo2dataco_batchesactionspost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `__key` | body | `object` | yes | Required key object for the change order batch. |
| `__key.KeyID` | body | `number` | yes | Required key ID for the batch to post. |
| `PostedDate` | body | `string` | no | Optional posting date in YYYY-MM-DD format. |
