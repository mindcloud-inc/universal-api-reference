# Add AP Invoice Batch with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ap/2/data/inv_batches/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add AP Invoice Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaap2datainv_batchesactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | AP company. Allowed range: 1 to 255. |
| `Mth` | body | `string` | yes | Posting month for the invoice batch. Format: YYYY-MM-01. |
| `Notes` | body | `string` | no | Optional notes for the invoice batch. |
