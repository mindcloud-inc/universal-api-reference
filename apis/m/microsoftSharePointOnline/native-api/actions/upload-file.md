# Upload File with Microsoft SharePoint Online

Uploads a file to Microsoft SharePoint Online.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.0/drives/{{driveId}}/root:/{{folderPath}}/{{fileName}}:/content`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Upload File](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID for the SharePoint document library. |
| `folderPath` | path | `string` | yes | Destination folder path under the drive root. Use an empty value for the root. |
| `fileName` | path | `string` | yes | Name to use for the uploaded file. |
| `content` | body | `file` | yes | File content to upload. |
