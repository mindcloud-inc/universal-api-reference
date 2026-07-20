# Get Contacts Report with Timetoreply

## Endpoint

- **Method:** `GET`
- **Path:** `/api/reports/contact`
- **Base URL:** `https://portal.timetoreply.com`
- **Official documentation:** [Get Contacts Report](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `model` | query | `string` | no | ID, name, email address, or domain to report on. |
| `model_type` | query | `string` | no | Model type for the selected model. |
| `search` | query | `string` | no | Search for a specific email subject line. |
| `to` | query | `string` | no | End date in YYYY-MM-DD format. |
