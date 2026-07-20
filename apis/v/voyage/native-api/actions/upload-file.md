# Upload File with Voyage

Uploads a file for Voyage batch processing.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files`
- **Base URL:** `https://api.voyageai.com`
- **Official documentation:** [Upload File](https://docs.voyageai.com/reference/upload-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | JSONL file object to upload for batch processing. |
| `purpose` | body | `list` | yes | Purpose for the uploaded file. Accepted values: `0`. |
