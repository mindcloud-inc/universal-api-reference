# List File Requests with Dropbox

Retrieves file requests for the current user from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_requests/list_v2`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [List File Requests](https://www.dropbox.com/developers/documentation/http/documentation#file_requests-list_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Maximum number of file requests to return. |
