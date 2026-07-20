# List Purchase Orders with BILL Payables & Receivables

Retrieves purchase orders from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/PurchaseOrder.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Purchase Orders](https://developer.bill.com/v2/reference/ap-vendortransactions-listpurchaseorders)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
