# Get Drive Item By Path with MS SharePoint

Retrieves a SharePoint drive item using it's path relative to the root folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/drives/:driveId/root:/:path`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Drive Item By Path](https://learn.microsoft.com/en-us/graph/api/driveitem-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID. |
| `path` | path | `string` | yes | Path relative to the root folder |
