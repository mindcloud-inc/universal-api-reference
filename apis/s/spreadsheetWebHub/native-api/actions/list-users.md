# List Users with SpreadsheetWeb Hub

Retrieves users from a SpreadsheetWeb Hub workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/list/:workspaceId`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [List Users](https://api.spreadsheetweb.com/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | SpreadsheetWeb workspace UUID. |
