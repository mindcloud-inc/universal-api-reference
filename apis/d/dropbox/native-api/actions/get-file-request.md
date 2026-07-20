# Get File Request with Dropbox

Retrieves a file request from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_requests/get`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Get File Request](https://www.dropbox.com/developers/documentation/http/documentation#file_requests-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the file request to retrieve. |
