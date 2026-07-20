# Delete File or Folder with Dropbox

Deletes an existing file or folder from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/delete_v2`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Delete File or Folder](https://www.dropbox.com/developers/documentation/http/documentation#files-delete_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | Dropbox path of the file or folder to delete. |
| `parent_rev` | body | `string` | no | Optional parent revision for safer deletes. |
