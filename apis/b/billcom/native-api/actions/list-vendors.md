# List Vendors with BILL Payables & Receivables

Retrieves vendors from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/Vendor.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Vendors](https://developer.bill.com/v2/reference/ap-vendormgmt-listvendor)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
