# Update File with File.io

Updates a file in File.io, retaining omitted fields.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/{{key}}`
- **Base URL:** `https://file.io`
- **Official documentation:** [Update File](https://www.file.io/developers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | File.io file key to update. |
| `file` | body | `file` | no | Optional file content to patch as multipart/form-data. |
| `expires` | body | `string` | no | Optional expiration duration to patch such as 1d, 1w, 1M, or 1y. |
| `maxDownloads` | body | `number` | no | Optional maximum download count to patch. |
| `autoDelete` | body | `boolean` | no | Optional auto-delete setting to patch. |
