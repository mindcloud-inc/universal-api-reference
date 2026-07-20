# Get Transaction Detail by Account with QuickBooks Online

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/TransactionDetailByAccount`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Get Transaction Detail by Account](https://developer.intuit.com/app/developer/qbo/docs/workflows/run-reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | Start date for the report period. Use YYYY-MM-DD format. |
| `end_date` | query | `string` | no | End date for the report period. Use YYYY-MM-DD format. |
| `accounting_method` | query | `list` | no | Accounting basis to use for the report. Accepted values: `0`, `1`. |
| `account` | query | `string` | no | QuickBooks account filter for the Transaction Detail by Account report. Use the QuickBooks account Id. |
| `vendor` | query | `string` | no | Optional QuickBooks vendor filter for the account detail report. |
| `customer` | query | `string` | no | Optional QuickBooks customer filter for the account detail report. |
