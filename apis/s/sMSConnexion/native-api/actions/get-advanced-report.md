# Get Advanced Report with SMS Connexion

Retrieves an advanced report from SMS Connexion.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Advanced Report](https://sms.cx/sms-api-documentation/#operation/GetAdvancedReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | query | `string` | no | Reporting period (YYYY-MM or YYYY). |
| `start_date` | query | `string` | no | Start date in YYYY-MM-DD. |
| `end_date` | query | `string` | no | End date in YYYY-MM-DD. |
