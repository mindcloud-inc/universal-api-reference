# Update Record with BILL Payables & Receivables

Updates a record in Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `Crud/Update/:recordType`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [Update Record](https://developer.bill.com/v2/reference/ap-vendormgmt-updatevendor)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recordType` | path | `string` | yes |
| `data` | body | `string` | no |
