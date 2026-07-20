# List Drive Root Items with MS SharePoint

Retrieves items from a SharePoint drive root folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/drives/{{driveId}}/root/children`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Drive Root Items](https://learn.microsoft.com/en-us/graph/api/driveitem-list-children?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID. |
