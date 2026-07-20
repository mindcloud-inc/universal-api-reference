# Delete Data Share Link with SpreadsheetWeb Hub

Deletes an existing data share link from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/datashare/delete`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Delete Data Share Link](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.dataShareLinkId` | body | `string` | yes | Identifier of the data share link to delete. |
| `request.applicationId` | body | `string` | yes | SpreadsheetWeb application identifier that owns the data share link. |
| `request.workspaceId` | body | `string` | yes | Workspace identifier that owns the data share link. |
