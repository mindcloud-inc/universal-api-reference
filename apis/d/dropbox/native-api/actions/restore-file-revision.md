# Restore File Revision with Dropbox

Restores a file revision in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/restore`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Restore File Revision](https://www.dropbox.com/developers/documentation/http/documentation#files-restore)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | Dropbox path for the file revision to restore. |
| `rev` | body | `string` | yes | Revision identifier to restore. |
