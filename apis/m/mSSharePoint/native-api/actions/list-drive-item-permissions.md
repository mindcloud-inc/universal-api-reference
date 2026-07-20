# List Drive Item Permissions with MS SharePoint

Retrieves permissions for a SharePoint drive item.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/drives/{{driveId}}/items/{{itemId}}/permissions`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Drive Item Permissions](https://learn.microsoft.com/en-us/graph/api/driveitem-list-permissions?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID. |
| `itemId` | path | `string` | yes | Drive item ID. |
