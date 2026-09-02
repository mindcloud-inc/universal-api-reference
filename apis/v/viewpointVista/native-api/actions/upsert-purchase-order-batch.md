# Upsert Purchase Order Batch with Viewpoint Vista

Upsert Purchase Order Batch

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/po/2/data/po_batches/actions/upsert`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Upsert Purchase Order Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapo2datapo_batchesactionsupsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista PR company. |
| `Mth` | body | `string` | yes | Posting month for the batch. Format: YYYY-MM-DD. |
| `Notes` | body | `string` | no | Optional notes for the timecard batch. Maximum length: 0. |
| `__batch` | body | `string` | no | — |
