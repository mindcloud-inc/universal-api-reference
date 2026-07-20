# List Bills with BILL Payables & Receivables

Retrieves bills from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/Bill.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Bills](https://developer.bill.com/v2/reference/ap-vendortransactions-listbill)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
