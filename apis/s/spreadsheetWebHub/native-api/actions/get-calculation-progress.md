# Get Calculation Progress with SpreadsheetWeb Hub

Retrieves calculation progress from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/calculations/getprogressstate`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Get Calculation Progress](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `string` | no | Async calculation progress UUID. |
| `keys` | body | `object` | no | Calculation key envelope. |
| `keys.applicationId` | body | `string` | no | SpreadsheetWeb application UUID. |
