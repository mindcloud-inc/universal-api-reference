# Add Change Order Batch with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/po/2/data/co_batches/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add Change Order Batch](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapo2dataco_batchesactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Company for the change order batch. |
| `Mth` | body | `string` | yes | Posting month in YYYY-MM-01 format. |
| `Notes` | body | `string` | no | Optional batch notes. |
