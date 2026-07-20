# Upload File with Dynalist

Uploads a file to Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Upload File](https://apidocs.dynalist.io/#upload-file-pro-only)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Filename to upload. |
| `content_type` | body | `string` | yes | MIME type for the upload. |
| `data` | body | `string` | yes | File data for the upload, matching Dynalist's documented `data` request field. |
