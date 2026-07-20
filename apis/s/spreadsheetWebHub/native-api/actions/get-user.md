# Get User with SpreadsheetWeb Hub

Retrieves a user from SpreadsheetWeb Hub.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/get/:workspaceId/:userId`
- **Base URL:** `https://api.spreadsheetweb.com`
- **Official documentation:** [Get User](https://api.spreadsheetweb.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | SpreadsheetWeb workspace UUID. |
| `userId` | path | `string` | yes | SpreadsheetWeb user UUID. |
