# Upload File with Microsoft 365

Uploads a file to Microsoft 365.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.0/me/drive/root\:/:folderPath/:fileName\:/content`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Upload File](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `file` | yes | — |
| `folderPath` | path | `string` | yes | Folder path where the file should be uploaded. |
| `fileName` | path | `string` | yes | Name of the uploaded file, including extension. |
