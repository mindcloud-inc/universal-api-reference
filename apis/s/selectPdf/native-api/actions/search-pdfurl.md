# Search PDF URL with SelectPdf

## Endpoint

- **Method:** `POST`
- **Path:** `/pdftotext/`
- **Base URL:** `https://selectpdf.com/api2`
- **Official documentation:** [Search PDF URL](https://selectpdf.com/pdf-to-text-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The public PDF URL to search. |
| `search_text` | body | `string` | yes | Text to search for inside the PDF. |
