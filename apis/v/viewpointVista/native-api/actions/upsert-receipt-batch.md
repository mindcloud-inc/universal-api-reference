# Upsert Receipt Batch with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ar/2/data/batches/actions/upsert_receipt`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Upsert Receipt Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatchesactionsupsert_receipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | AR company for the receipt batch. |
| `Mth` | body | `string` | yes | Posting month for the receipt batch. Format: YYYY-MM-01. |
| `Notes` | body | `string` | no | Optional notes for the receipt batch. |
| `__batch` | body | `string` | no | Batch Custom ID. |
