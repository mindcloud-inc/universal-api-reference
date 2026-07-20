# List Users with BILL Payables & Receivables

Retrieves users from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/User.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Users](https://developer.bill.com/v2/reference/org-basic-listuser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
