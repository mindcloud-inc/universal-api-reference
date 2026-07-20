# Get Report Summary with SMS Connexion

Retrieves summary reports by dimension from SMS Connexion.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/summary/:dimension`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Report Summary](https://sms.cx/sms-api-documentation/#operation/GetSummaryReports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimension` | path | `string` | yes | Summary dimension. Accepted values: source, channel, country, traffic, delivery. |
| `period` | query | `string` | no | Reporting period (YYYY-MM or YYYY). |
| `start_date` | query | `string` | no | Start date in YYYY-MM-DD. |
| `end_date` | query | `string` | no | End date in YYYY-MM-DD. |
