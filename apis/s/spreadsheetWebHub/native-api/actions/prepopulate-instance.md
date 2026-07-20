# Prepopulate Instance with SpreadsheetWeb Hub

Prepopulates an application instance in SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/calculations/prepopulateinstance`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Prepopulate Instance](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Primary request payload. |
| `request.applicationId` | body | `string` | no | SpreadsheetWeb application UUID. |
| `request.inputs[]` | body | `array<object>` | no | Prepopulation inputs. |
