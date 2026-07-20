# List File Revisions with Dropbox

Retrieves revision history for a file from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/list_revisions`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [List File Revisions](https://www.dropbox.com/developers/documentation/http/documentation#files-list_revisions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | The file path or ID to list revisions for. |
