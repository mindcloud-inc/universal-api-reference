# Create Record with BILL Payables & Receivables

Creates a record in Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `Crud/Create/:recordType`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [Create Record](https://developer.bill.com/v2/reference/ap-vendortransactions-createpurchaseorder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recordType` | path | `string` | yes |
| `data` | body | `string` | no |
