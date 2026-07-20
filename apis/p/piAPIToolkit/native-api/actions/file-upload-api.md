# File Upload API with PiAPI/Toolkit

Uploads a file for PiAPI/Toolkit tasks.

## Endpoint

- **Method:** `POST`
- **Path:** `https://upload.theapi.app/api/ephemeral_resource`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [File Upload API](https://piapi.ai/docs/tools/file-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Original filename to associate with the uploaded file. |
| `file_data` | body | `string` | yes | Base64-encoded file content expected by PiAPI. |
