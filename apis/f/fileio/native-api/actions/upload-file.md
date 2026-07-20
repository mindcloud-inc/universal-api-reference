# Upload File with File.io

Uploads a file to File.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://file.io`
- **Official documentation:** [Upload File](https://www.file.io/developers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File to upload as multipart/form-data. Required by File.io for file upload. |
| `expires` | body | `string` | no | Optional expiration duration such as 1d, 1w, 1M, or 1y. |
| `maxDownloads` | body | `number` | no | Optional maximum number of downloads before the file expires. |
| `autoDelete` | body | `boolean` | no | Whether File.io should automatically delete the file after download or expiration. |
