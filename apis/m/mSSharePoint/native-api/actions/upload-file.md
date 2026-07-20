# Upload File with MS SharePoint

Uploads a file to SharePoint.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.0/drives/{{driveId}}/root:/{{folderPath}}/{{fileName}}:/content`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Upload File](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID. |
| `folderPath` | path | `string` | yes | Folder path relative to the drive root. |
| `fileName` | path | `string` | yes | Name of the file to upload. |
| `file` | body | `string` | yes | Raw content to upload as the file body. |
