# Add Credit Memo with Viewpoint Vista

Adds a Non-Contract based invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ar/2/data/batch_entries/actions/add_credit_memo`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add Credit Memo](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2databatch_entriesactionsadd_non-contract_inv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista PR company. |
| `Mth` | body | `string` | yes | Posting month for the batch. Format: YYYY-MM-DD. |
| `BatchId` | body | `number` | yes | — |
| `TransDate` | body | `string` | yes | — |
| `Invoice` | body | `string` | no | — |
| `CustRef` | path | `string` | no | — |
| `Description` | body | `string` | no | — |
| `ReasonCode` | body | `string` | no | — |
| `Notes` | body | `string` | no | — |
| `MiscDistributions[]` | body | `array` | no | — |
| `LineItems[]` | body | `array` | no | — |
| `__custom_fields` | body | `object` | no | — |
| `AppliedMth` | body | `string` | no | — |
| `AppliedTrans` | body | `number` | no | — |
| `ARLine` | body | `number` | no | — |
| `LineType` | body | `string` | no | — |
| `__BaseAmount` | body | `string` | no | — |
| `GLAcct` | body | `string` | no | — |
