# Update File Request with Dropbox

Updates an existing file request in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_requests/update`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Update File Request](https://www.dropbox.com/developers/documentation/http/documentation#file_requests-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the file request to update. |
| `title` | body | `string` | no | Updated title for the file request. |
| `destination` | body | `string` | no | Updated Dropbox folder path for uploaded files. |
| `deadline.deadline` | body | `string` | no | Updated deadline in RFC 3339 format. |
| `deadline.allow_late_uploads` | body | `boolean` | no | Allow uploads after the updated deadline passes. |
| `open` | body | `boolean` | no | Whether the file request should remain open. |
| `description` | body | `string` | no | Updated description shown to request participants. |
