# Upload PDF File with ChatPDF

## Endpoint

- **Method:** `POST`
- **Path:** `/sources/add-file`
- **Base URL:** `https://api.chatpdf.com/v1`
- **Official documentation:** [Upload PDF File](https://www.chatpdf.com/docs/api/backend)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF file to upload to ChatPDF. |
