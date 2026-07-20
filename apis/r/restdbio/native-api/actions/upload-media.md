# Upload Media with Restdb.io

Uploads media files to Restdb.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/media`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Upload Media](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | body | `string` | yes | Multipart form-data payload with one or more files. |
