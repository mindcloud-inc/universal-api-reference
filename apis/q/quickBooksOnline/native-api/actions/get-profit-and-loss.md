# Get Profit and Loss with QuickBooks Online

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/ProfitAndLoss`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Get Profit and Loss](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/profitandloss)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | no | Start date for the report period. Use YYYY-MM-DD format. |
| `end_date` | query | `string` | no | End date for the report period. Use YYYY-MM-DD format. |
| `accounting_method` | query | `list` | no | Accounting basis to use for the report, such as Cash or Accrual. Accepted values: `0`, `1`. |
| `summarize_column_by` | query | `list` | no | Column grouping for the report, such as Total, Month, or Customers. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `customer` | query | `string` | no | Optional QuickBooks customer ID filter. |
| `vendor` | query | `string` | no | Optional QuickBooks vendor ID filter. |
| `class` | query | `string` | no | Optional QuickBooks class ID filter. |
| `department` | query | `string` | no | Optional QuickBooks department ID filter. |
