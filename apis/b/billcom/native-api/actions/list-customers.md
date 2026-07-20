# List Customers with BILL Payables & Receivables

Retrieves customers from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/Customer.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Customers](https://developer.bill.com/v2/reference/ar-customermgmt-listcustomer)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
