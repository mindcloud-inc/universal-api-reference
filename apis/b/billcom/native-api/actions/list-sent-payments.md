# List Sent Payments with BILL Payables & Receivables

Retrieves sent payments from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/SentPay.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Sent Payments](https://developer.bill.com/v2/reference/ap-vendortransactions-listsentpay)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
