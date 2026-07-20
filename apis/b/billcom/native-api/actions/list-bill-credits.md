# List Bill Credits with BILL Payables & Receivables

Retrieves bill credits from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/BillCredit.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Bill Credits](https://developer.bill.com/v2/reference/ap-vendortransactions-listbillcredit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
