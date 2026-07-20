# List Applications with SpreadsheetWeb Hub

Retrieves applications from a SpreadsheetWeb Hub workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/list/:workspaceId/:onlyPublishedWithDatabases`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [List Applications](https://api.spreadsheetweb.com/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The target workspace identifier. |
| `onlyPublishedWithDatabases` | path | `boolean` | yes | When true, list only applications that have databases and published transactions. |
