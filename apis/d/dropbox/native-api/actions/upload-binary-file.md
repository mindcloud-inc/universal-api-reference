# Upload Binary File with Dropbox

## Endpoint

- **Method:** `POST`
- **Path:** `https://content.dropboxapi.com/2/files/upload`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Upload Binary File](https://docs.dropboxapi.com/dropbox-api/api-reference/user-endpoints/files/upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | — |
| `file` | body | `file` | yes | Base64-encoded file content or an accessible HTTP(S) download URL. Sends the original bytes as the request body. Maximum 100 MiB. |
| `mode` | query | `list<string>` | no | Add creates a file; overwrite replaces existing content. Revision-conditional update is not supported by this action. Accepted values: `add`, `overwrite`. |
| `autorename` | query | `boolean` | no | — |
| `mute` | query | `boolean` | no | — |
| `strict_conflict` | query | `boolean` | no | — |
