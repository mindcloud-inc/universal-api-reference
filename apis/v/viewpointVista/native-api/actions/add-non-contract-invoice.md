# Add Non-Contract Invoice with Viewpoint Vista

Adds a Non-Contract based invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/pr/2/data/batch_entries/actions/add_non-contract_inv`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add Non-Contract Invoice](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batchesactionsupsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista PR company. |
| `Mth` | body | `string` | yes | Posting month for the batch. Format: YYYY-MM-DD. |
| `BatchId` | body | `string` | yes | — |
| `CustGroup` | body | `string` | yes | — |
| `Customer` | body | `string` | yes | — |
| `RecType` | body | `number` | no | — |
| `CustRef` | path | `string` | no | — |
| `Invoice` | body | `string` | no | — |
| `Description` | body | `string` | no | — |
| `TransDate` | body | `string` | yes | — |
| `DiscDate` | body | `string` | no | — |
| `ReasonCode` | body | `string` | no | — |
| `Notes` | body | `string` | no | — |
| `__custom_fields` | body | `object` | no | — |
| `MiscDistributions[]` | body | `array` | no | — |
| `LineItems[]` | body | `array` | no | — |
