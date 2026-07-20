# Get Report XLSX Export with SMS Connexion

Retrieves an advanced report export from SMS Connexion as XLSX.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/xlsx`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Report XLSX Export](https://sms.cx/sms-api-documentation/#operation/ExportAdvancedReportToXLSX)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | query | `string` | no | Reporting period (YYYY-MM or YYYY). |
| `start_date` | query | `string` | no | Start date in YYYY-MM-DD. |
| `end_date` | query | `string` | no | End date in YYYY-MM-DD. |
