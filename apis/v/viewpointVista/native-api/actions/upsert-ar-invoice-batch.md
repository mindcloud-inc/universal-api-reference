# Upsert AR Invoice Batch with Viewpoint Vista

Upsert Invoice Batch

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ap/2/data/inv_batches/actions/upsert`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Upsert AR Invoice Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista PR company. |
| `Mth` | body | `string` | yes | Posting month for the batch. Format: YYYY-MM-DD. |
| `Notes` | body | `string` | no | Optional notes for the timecard batch. Maximum length: 0. |
| `__batch` | body | `string` | no | — |
| `__lockBatch` | body | `boolean` | no | Keep the batch locked after processing the action |
