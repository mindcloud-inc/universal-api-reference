# Create Folder with Dropbox

Creates a new folder in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/create_folder_v2`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Create Folder](https://www.dropbox.com/developers/documentation/http/documentation#files-create_folder_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | Path in Dropbox where the folder should be created. |
| `autorename` | body | `boolean` | no | If true, Dropbox tries to rename the folder when the target path conflicts. |
