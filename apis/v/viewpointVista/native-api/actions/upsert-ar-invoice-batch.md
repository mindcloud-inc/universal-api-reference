# Upsert AR Invoice Batch with Viewpoint Vista

Upsert Invoice Batch

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ar/2/data/batches/actions/add_invoice`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Upsert AR Invoice Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatchesactionsadd_invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista PR company. |
| `Mth` | body | `string` | yes | Posting month for the batch. Format: YYYY-MM-DD. |
| `Notes` | body | `string` | no | Optional notes for the timecard batch. Maximum length: 0. |
