# Add PO Purchase Order with Viewpoint Vista

Adds a Purchase Order

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/po/2/data/po_batch_entries/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add PO Purchase Order](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapo2datapo_batch_entriesactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Vista PR company. |
| `Mth` | body | `string` | yes | Posting month for the batch. Format: YYYY-MM-DD. |
| `BatchId` | body | `number` | yes | — |
| `PO` | body | `string` | yes | — |
| `Vendor` | body | `number` | yes | — |
| `Description` | body | `string` | no | — |
| `OrderDate` | body | `string` | no | — |
| `OrderedBy` | body | `string` | no | — |
| `ExpDate` | body | `string` | no | — |
| `Status` | body | `number` | no | Options: 0-Open, 1-Complete, 2-Close. Optional. If omitted, 0 will be defaulted. |
| `JCCo` | body | `number` | no | — |
| `Job` | body | `string` | no | — |
| `INCo` | body | `number` | no | — |
| `Loc` | body | `string` | no | — |
| `ShipLoc` | body | `string` | no | — |
| `ShipAddress` | body | `object` | no | — |
| `PayTerms` | body | `string` | no | — |
| `Notes` | body | `string` | no | — |
| `WorkOrder` | body | `number` | no | — |
| `__custom_fields` | body | `object` | no | — |
| `LineItems[]` | body | `array` | no | — |
