# Add Receipt Batch with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ar/2/data/batches/actions/add_receipt`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add Receipt Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatchesactionsadd_receipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | AR company for the receipt batch. Allowed range: 1 to 255. |
| `Mth` | body | `date` | yes | Posting month for the receipt batch. Format: YYYY-MM-01. |
| `Notes` | body | `string` | no | Optional notes for the receipt batch. |
