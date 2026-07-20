# Get Productivity Report with Timetoreply

## Endpoint

- **Method:** `GET`
- **Path:** `/api/reports/productivity`
- **Base URL:** `https://portal.timetoreply.com`
- **Official documentation:** [Get Productivity Report](https://portal.timetoreply.com/api-docs#reports-GETapi-reports-productivity)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Reference date for the productivity report. |
| `model` | query | `string` | no | ID, name, email address, or domain to report on. |
| `model_type` | query | `string` | no | Model type for the selected model. |
