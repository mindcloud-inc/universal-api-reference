# Delete Tag with SpreadsheetWeb Hub

Deletes an existing tag from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/delete`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Delete Tag](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Primary request payload. |
| `request.workspaceId` | body | `string` | no | SpreadsheetWeb workspace UUID. |
| `request.tagId` | body | `string` | no | SpreadsheetWeb tag UUID. |
| `request.text` | body | `string` | yes | Tag label text. |
