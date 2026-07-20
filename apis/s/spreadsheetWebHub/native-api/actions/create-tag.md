# Create Tag with SpreadsheetWeb Hub

Creates a new tag in SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/create`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Create Tag](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Primary request payload. |
| `request.workspaceId` | body | `string` | no | SpreadsheetWeb workspace UUID. |
| `request.text` | body | `string` | yes | Tag label text. |
| `request.type` | body | `number` | no | Tag type enum value. |
