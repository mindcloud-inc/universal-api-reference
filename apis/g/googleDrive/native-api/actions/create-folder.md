# Create Folder with Google Drive

Creates a new Folder in Google Drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v3/files`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Create Folder](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Give the new Folder a name. |
| `parents` | body | `list<string>` | no | The ID of a Google Drive Folder to place your file. When not specified files are added to your My Drive. Send multiple values as a array. |
