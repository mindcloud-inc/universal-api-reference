# Continue Folder Listing with Dropbox

Retrieves more Dropbox folder contents using a cursor.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/list_folder/continue`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Continue Folder Listing](https://www.dropbox.com/developers/documentation/http/documentation#files-list_folder/continue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | body | `string` | yes | The cursor returned by a previous folder listing call. |
