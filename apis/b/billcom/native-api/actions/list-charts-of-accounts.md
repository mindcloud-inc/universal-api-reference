# List Charts of Accounts with BILL Payables & Receivables

Retrieves chart of accounts from Bill.com.

## Endpoint

- **Method:** `POST`
- **Path:** `List/ChartOfAccount.json`
- **Base URL:** `https://api.bill.com/api/v2`
- **Official documentation:** [List Charts of Accounts](https://developer.bill.com/v2/reference/org-accounts-listchartofaccount)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters[]` | body | `array` | no |
| `filters[].field` | body | `string` | no |
| `filters[].op` | body | `list` | no |
| `filters[].value` | body | `string` | no |
