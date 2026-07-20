# Extract Text From File with PDF API Hub

## Endpoint

- **Method:** `POST`
- **Path:** `/extract-text`
- **Base URL:** `https://api.prefillpdf.com`
- **Official documentation:** [Extract Text From File](https://api.prefillpdf.com/docs#/PDF%20Tools/extract_text_endpoint_extract_text_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF file upload; can also be a public PDF URL |
| `inline` | query | `boolean` | no | Return text inline instead of file |
