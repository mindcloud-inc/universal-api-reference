# Upload File with Dropbox

Uploads a new file to Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `https://content.dropboxapi.com/2/files/upload`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Upload File](https://www.dropbox.com/developers/documentation/http/documentation#files-upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | Dropbox path where the file will be uploaded. |
| `content` | body | `string` | yes | UTF-8 file content to upload. |
| `mode` | body | `string` | no | Write mode for the upload. Use add to create a new file or overwrite to replace the current content. Accepted values: `0`, `1`. |
| `autorename` | body | `boolean` | no | Automatically rename the file on conflict. |
| `mute` | body | `boolean` | no | Suppress notifications for the file update. |
| `strict_conflict` | body | `boolean` | no | Reject writes unless Dropbox can apply the exact requested mode. |
