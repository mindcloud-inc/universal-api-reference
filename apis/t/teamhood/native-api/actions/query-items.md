# Query Items with Teamhood

Finds items in Teamhood by query filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/items`
- **Base URL:** `https://api-mindcloud1.teamhood.com/api/v1`
- **Official documentation:** [Query Items](https://api-mindcloud1.teamhood.com/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AssignedUserId` | query | `string` | no | Filter items by assignee. |
| `BoardId` | query | `string` | no | Filter items by board. |
| `Completed` | query | `string` | no | Filter completed items. |
| `CompletedSince` | query | `string` | no | Filter items completed since the given ISO timestamp. |
| `CreatedSince` | query | `string` | no | Filter items created since the given ISO timestamp. |
| `IncludeChildItems` | query | `string` | no | Include child items in the response. |
| `ModifiedSince` | query | `string` | no | Filter items modified since the given ISO timestamp. |
| `OwnerId` | query | `string` | no | Filter items by owner. |
| `ParentId` | query | `string` | no | Filter child items by parent item. |
| `RowId` | query | `string` | no | Filter items by row. |
| `Skip` | query | `string` | no | Number of items to skip. |
| `StatusId` | query | `string` | no | Filter items by status. |
| `Take` | query | `string` | no | Number of items to return. |
| `WorkspaceId` | query | `string` | no | Filter items by workspace. |
