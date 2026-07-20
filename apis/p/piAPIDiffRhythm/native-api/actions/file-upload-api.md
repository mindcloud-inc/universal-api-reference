# File Upload API with PiAPI/DiffRhythm

Creates a temporary file upload in PiAPI/DiffRhythm.

## Endpoint

- **Method:** `POST`
- **Path:** `https://upload.theapi.app/api/ephemeral_resource`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [File Upload API](https://piapi.ai/docs/tools/file-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | File name including a supported extension such as `.mp3`, `.wav`, `.png`, or `.jpg`. |
| `file_data` | body | `string` | yes | Base64-encoded file content. PiAPI also accepts a matching data URI. |
