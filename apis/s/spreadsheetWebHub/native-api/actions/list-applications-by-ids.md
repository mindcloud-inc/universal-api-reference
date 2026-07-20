# List Applications by IDs with SpreadsheetWeb Hub

Retrieves multiple applications from SpreadsheetWeb Hub by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/getmany`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [List Applications by IDs](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Primary request payload. |
| `request.workspaceId` | body | `string` | no | SpreadsheetWeb workspace UUID. |
| `secondaryRequest[]` | body | `array<string>` | no | Application UUIDs to fetch in bulk. |
