# List Invoices with BILL Payables & Receivables

Retrieves invoices from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/Invoice.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Invoices](https://developer.bill.com/v2/reference/ar-customertransactions-listinvoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
