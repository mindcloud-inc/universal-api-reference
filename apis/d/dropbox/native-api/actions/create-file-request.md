# Create File Request with Dropbox

Creates a file request in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_requests/create`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Create File Request](https://www.dropbox.com/developers/documentation/http/documentation#file_requests-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title shown on the file request page. |
| `destination` | body | `string` | yes | Dropbox folder path where uploaded files should be stored. |
| `deadline.deadline` | body | `string` | no | Deadline for the file request in RFC 3339 format. |
| `deadline.allow_late_uploads` | body | `boolean` | no | Allow uploads after the deadline passes. |
| `open` | body | `boolean` | no | Whether the file request should be open after creation. |
| `description` | body | `string` | no | Optional description shown to request participants. |
