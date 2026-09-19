# Add Change Order Batch Entry with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/po/2/data/co_batch_entries/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add Change Order Batch Entry](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapo2dataco_batch_entriesactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | Company. Key to the change order batch. |
| `Mth` | body | `string` | yes | Batch posting month in YYYY-MM-01 format. |
| `BatchId` | body | `number` | yes | Change order batch ID. |
| `POCONum` | body | `number` | no | Optional PO change order number; the next available number is used when omitted. |
| `ChangeOrder` | body | `string` | no | Optional change order number used to group related changes. |
| `ActDate` | body | `string` | no | Optional action date in YYYY-MM-DD format. |
| `PO` | body | `string` | yes | Purchase order number. |
| `POItem` | body | `number` | yes | Purchase order line item number. |
| `Description` | body | `string` | no | Optional change description. |
| `ChangeCurUnits` | body | `string` | no | Optional change to current units for non-LS items. |
| `ChangeBOUnits` | body | `string` | no | Optional change to backorder units for non-LS items. |
| `ChangeCurCost` | body | `string` | no | Optional change to current cost for LS items. |
| `ChangeBOCost` | body | `string` | no | Optional change to backorder cost for LS items. |
| `NewLineItem` | body | `object` | no | Optional details used when adding a new PO line item. |
| `Notes` | body | `string` | no | Optional entry notes. |
| `__custom_fields` | body | `object` | no | Optional Vista user-defined fields, keyed by field name. |
