# List Workspace Users with Testlify

Retrieves workspace users from Testlify with optional filters and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workspace/team`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [List Workspace Users](https://docs.testlify.com/reference/get_workspace_users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search query string. |
| `userStatus` | query | `string` | no | Filter by workspace user status. |
| `userRole` | query | `string` | no | Filter by workspace user role. |
| `userRoleId` | query | `string` | no | Filter by user role identifier. |
| `colName` | query | `string` | no | Column name to sort by. |
| `inOrder` | query | `string` | no | Sort order. |
| `limit` | query | `number` | no | Number of items to return. |
| `skip` | query | `number` | no | Number of items to skip. |
