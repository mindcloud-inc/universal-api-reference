# Upload File with Instant

Uploads a file to Instant storage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/storage/upload`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Upload File](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File content to upload. |
| `path` | body | `string` | yes | Storage path to write the file to. |
| `contentType` | body | `string` | no | MIME type to send for the uploaded file. |
