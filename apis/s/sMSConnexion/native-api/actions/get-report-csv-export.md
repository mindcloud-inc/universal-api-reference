# Get Report CSV Export with SMS Connexion

Retrieves an advanced report export from SMS Connexion as CSV.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/csv`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Report CSV Export](https://sms.cx/sms-api-documentation/#operation/ExportAdvancedReportToCSV)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | query | `string` | no | Reporting period (YYYY-MM or YYYY). |
| `start_date` | query | `string` | no | Start date in YYYY-MM-DD. |
| `end_date` | query | `string` | no | End date in YYYY-MM-DD. |
