# Get Transaction List with QuickBooks Online

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/TransactionList`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Get Transaction List](https://developer.intuit.com/app/developer/qbo/docs/workflows/run-reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | Start date for the report period. Use YYYY-MM-DD format. |
| `end_date` | query | `string` | no | End date for the report period. Use YYYY-MM-DD format. |
| `accounting_method` | query | `list` | no | Accounting basis to use for the report. Accepted values: `0`, `1`. |
| `vendor` | query | `string` | no | Optional QuickBooks vendor filter for the transaction report. |
| `customer` | query | `string` | no | Optional QuickBooks customer filter for the transaction report. |
