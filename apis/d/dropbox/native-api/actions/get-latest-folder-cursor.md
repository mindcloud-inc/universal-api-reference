# Get Latest Folder Cursor with Dropbox

Retrieves the latest cursor for a Dropbox folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/list_folder/get_latest_cursor`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Get Latest Folder Cursor](https://www.dropbox.com/developers/documentation/http/documentation#files-list_folder/get_latest_cursor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | The folder path or ID to get a latest cursor for. Leave blank to use the root folder. |
