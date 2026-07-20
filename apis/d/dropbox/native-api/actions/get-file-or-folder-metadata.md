# Get File or Folder Metadata with Dropbox

Retrieves file or folder metadata from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/get_metadata`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Get File or Folder Metadata](https://www.dropbox.com/developers/documentation/http/documentation#files-get_metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | The file or folder path or ID to fetch metadata for. |
