# List Workspace Invites with SpreadsheetWeb Hub

Retrieves workspace invites from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/invites/workspacelist/:workspaceId`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [List Workspace Invites](https://api.spreadsheetweb.com/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | SpreadsheetWeb workspace UUID. |
