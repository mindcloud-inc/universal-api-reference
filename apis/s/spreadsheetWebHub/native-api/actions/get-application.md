# Get Application with SpreadsheetWeb Hub

Retrieves an application from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/get/:applicationId/:workspaceId`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Get Application](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicationId` | path | `string` | yes | The target application identifier. |
| `workspaceId` | path | `string` | yes | The target workspace identifier. |
