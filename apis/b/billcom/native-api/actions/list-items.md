# List Items with BILL Payables & Receivables

Retrieves items from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/Item.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Items](https://developer.bill.com/v2/reference/org-accounts-listitem)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
