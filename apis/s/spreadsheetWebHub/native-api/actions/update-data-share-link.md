# Update Data Share Link with SpreadsheetWeb Hub

Updates an existing data share link in SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/datashare/update`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Update Data Share Link](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.dataShareLinkId` | body | `string` | yes | Identifier of the data share link to update. |
| `request.applicationId` | body | `string` | yes | SpreadsheetWeb application identifier that owns the data share link. |
| `request.workspaceId` | body | `string` | yes | Workspace identifier that owns the data share link. |
