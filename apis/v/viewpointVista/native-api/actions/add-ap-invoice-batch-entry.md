# Add AP Invoice Batch Entry with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/ap/2/data/inv_batch_entries/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add AP Invoice Batch Entry](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaap2datainv_batch_entriesactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Co` | body | `number` | yes | AP company. Allowed range: 1 to 255. |
| `Mth` | body | `string` | yes | Invoice batch posting month. Format: YYYY-MM-01. |
| `BatchId` | body | `number` | yes | Invoice batch ID. Key to ap/inv_batches(Co, Mth, BatchId). |
| `Vendor` | body | `number` | yes | Vendor ID. The vendor group defaults from Co. |
| `APRef` | body | `string` | yes | Invoice number. Maximum 30 characters. Maximum length: 30. |
| `Description` | body | `string` | no | Optional invoice description. Maximum 30 characters. Maximum length: 30. |
| `InvDate` | body | `string` | yes | Invoice date. Format: YYYY-MM-DD. |
| `DiscDate` | body | `string` | no | Optional discount date. Format: YYYY-MM-DD. |
| `DueDate` | body | `string` | no | Optional due date. Defaults from the vendor's payment terms when omitted. Format: YYYY-MM-DD. |
| `InvTotal` | body | `string` | no | Optional invoice total. When omitted, Trimble calculates it from the line items. |
| `PaymentOverride` | body | `object` | no | Optional payment override object. Use the documented PaymentOverride fields. |
| `AddressOverride` | body | `object` | no | Optional address override object. Use the documented AddressOverride fields. |
| `Notes` | body | `string` | no | Optional invoice notes. |
| `__custom_fields` | body | `object` | no | Optional Vista user-defined fields, keyed by the Vista field name. |
| `__disable_validation` | body | `boolean` | no | Optional. Disables Vista validations for this request. |
| `LineItems[]` | body | `array<object>` | yes | Required array with at least one AP line item object. Each item must use one supported Trimble LineType (1 through 8) and its documented fields. |
