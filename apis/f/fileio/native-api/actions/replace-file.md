# Replace File with File.io

Updates a file in File.io, resetting omitted fields.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{{key}}`
- **Base URL:** `https://file.io`
- **Official documentation:** [Replace File](https://www.file.io/developers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | File.io file key to replace. |
| `file` | body | `file` | no | Replacement file content as multipart/form-data. |
| `expires` | body | `string` | no | Optional replacement expiration duration such as 1d, 1w, 1M, or 1y. |
| `maxDownloads` | body | `number` | no | Optional replacement maximum download count. |
| `autoDelete` | body | `boolean` | no | Optional replacement auto-delete setting. |
