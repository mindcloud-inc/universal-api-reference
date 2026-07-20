# Create Data Share Link with SpreadsheetWeb Hub

Creates a new data share link in SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/datashare/create`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Create Data Share Link](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.applicationId` | body | `string` | yes | SpreadsheetWeb application identifier that owns the record to share. |
| `request.workspaceId` | body | `string` | yes | Workspace identifier that owns the record to share. |
| `request.recordId` | body | `number` | yes | SpreadsheetWeb record identifier to expose through the data share link. |
| `request.actionType` | body | `number` | yes | 0 for edit-mode links, 1 for view-mode links. |
