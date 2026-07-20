# Get Trend Report with Timetoreply

## Endpoint

- **Method:** `GET`
- **Path:** `/api/reports/trend`
- **Base URL:** `https://portal.timetoreply.com`
- **Official documentation:** [Get Trend Report](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-trend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Starting date for the trend report. |
| `model` | query | `string` | no | ID, name, email address, or domain to report on. |
| `model_type` | query | `string` | no | Model type for the selected model. |
| `period_type` | query | `string` | no | Period unit for the trend report. |
| `periods` | query | `number` | no | Number of periods to include. |
