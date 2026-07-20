# List Vendor Credits with BILL Payables & Receivables

Retrieves vendor credits from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/VendorCredit.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Vendor Credits](https://developer.bill.com/v2/reference/ap-vendortransactions-listvendorcredit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
