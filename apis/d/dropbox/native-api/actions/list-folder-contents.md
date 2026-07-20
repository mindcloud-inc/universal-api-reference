# List Folder Contents with Dropbox

Retrieves the contents of a Dropbox folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/list_folder`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [List Folder Contents](https://www.dropbox.com/developers/documentation/http/documentation#files-list_folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | The folder path or ID to list. Leave blank to list the root folder. |
