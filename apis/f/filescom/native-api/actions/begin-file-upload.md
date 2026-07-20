# Begin File Upload with Files.com

Begins a file upload in Files.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/file_actions/begin_upload/:path`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Begin File Upload](https://developers.files.com/rest/files/files#upload-file-optimized)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | Path of the file to upload, including file name. |
| `size` | query | `number` | yes | Total file size in bytes. |
| `mkdir_parents` | query | `boolean` | no | Create missing parent folders automatically when true. |
| `part` | query | `number` | no | Specific multipart upload part number to begin. |
| `parts` | query | `number` | no | Total number of multipart upload parts. |
| `ref` | query | `string` | no | Resume token from a previous begin-upload response. |
| `restart` | query | `number` | no | Restart the upload sequence from a given part index. |
| `with_rename` | query | `boolean` | no | Allow Files.com to rename the uploaded file to avoid conflicts. |
