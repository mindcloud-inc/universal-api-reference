# List Data Share Links with SpreadsheetWeb Hub

Retrieves data share links from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/datashare/list/:workspaceId/:applicationId/:dataId`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [List Data Share Links](https://api.spreadsheetweb.com/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | SpreadsheetWeb workspace UUID. |
| `applicationId` | path | `string` | yes | SpreadsheetWeb application UUID. |
| `dataId` | path | `number` | yes | SpreadsheetWeb record data identifier. |
