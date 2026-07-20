# List Application Tag Relationships with SpreadsheetWeb Hub

Retrieves application tag relationships from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/gettagrelationships/:applicationId/:workspaceId`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [List Application Tag Relationships](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicationId` | path | `string` | yes | The target application identifier. |
| `workspaceId` | path | `string` | yes | The target workspace identifier. |
