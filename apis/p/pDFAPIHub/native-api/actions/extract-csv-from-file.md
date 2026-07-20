# Extract CSV From File with PDF API Hub

## Endpoint

- **Method:** `POST`
- **Path:** `/extract-csv`
- **Base URL:** `https://api.prefillpdf.com`
- **Official documentation:** [Extract CSV From File](https://api.prefillpdf.com/docs#/PDF%20Tools/extract_csv_endpoint_extract_csv_post)

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
