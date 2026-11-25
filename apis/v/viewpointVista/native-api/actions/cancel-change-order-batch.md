# Cancel Change Order Batch with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/po/2/data/co_batches/actions/cancel`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Cancel Change Order Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapo2dataco_batchesactionscancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista company for the change order batch. Allowed range: 1 to 255. |
| `Mth` | body | `string` | yes | Posting month for the batch. Format: YYYY-MM-01. |
| `BatchId` | body | `number` | yes | Change order batch ID to cancel. |
| `__clearBatch` | body | `boolean` | no | When true, clears entries in the batch before cancellation. Omit or set false to fail when entries remain. |
