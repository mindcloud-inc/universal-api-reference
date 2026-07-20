# Get Temporary Link with Dropbox

Retrieves a temporary download link from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/get_temporary_link`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Get Temporary Link](https://www.dropbox.com/developers/documentation/http/documentation#files-get_temporary_link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | The file path or ID to get a temporary link for. |
