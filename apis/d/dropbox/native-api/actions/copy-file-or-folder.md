# Copy File or Folder with Dropbox

Creates a copy of a file or folder in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/copy_v2`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Copy File or Folder](https://www.dropbox.com/developers/documentation/http/documentation#files-copy_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_path` | body | `string` | yes | Source Dropbox path to copy. |
| `to_path` | body | `string` | yes | Destination Dropbox path for the copy. |
| `autorename` | body | `boolean` | no | Automatically rename the copied item on conflict. |
