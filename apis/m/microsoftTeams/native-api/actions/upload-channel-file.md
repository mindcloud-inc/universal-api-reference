# Upload Channel File with Microsoft Teams

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.0/drives/:driveId/items/:folderId:/:fileName:/content`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Upload Channel File](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Use parentReference.driveId returned by Get Channel Files Folder. |
| `folderId` | path | `string` | yes | Use id returned by Get Channel Files Folder. Do not use the channel ID. |
| `fileName` | path | `string` | yes | Destination file name, including extension. An existing file with this name is replaced. |
| `content` | body | `file` | yes | Base64 file content or a direct HTTPS download URL. The file is uploaded as binary bytes using this Teams connection. |
