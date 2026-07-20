# Download File with Dropbox

Retrieves a file's contents from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `https://content.dropboxapi.com/2/files/download`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Download File](https://www.dropbox.com/developers/documentation/http/documentation#files-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | The path or file id of the file to download. |
