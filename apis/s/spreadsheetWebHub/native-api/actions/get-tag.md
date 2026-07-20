# Get Tag with SpreadsheetWeb Hub

Retrieves a tag from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/get/:tagId/:workspaceId`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Get Tag](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `string` | yes | SpreadsheetWeb tag UUID. |
| `workspaceId` | path | `string` | yes | SpreadsheetWeb workspace UUID. |
