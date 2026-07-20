# Get Application by Slug with SpreadsheetWeb Hub

Retrieves an application from SpreadsheetWeb Hub by slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/getbyslug/:applicationSlug/:workspaceId`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Get Application by Slug](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicationSlug` | path | `string` | yes | The target application slug. |
| `workspaceId` | path | `string` | yes | The target workspace identifier. |
