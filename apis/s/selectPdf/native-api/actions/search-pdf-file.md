# Search PDF File with SelectPdf

## Endpoint

- **Method:** `POST`
- **Path:** `/pdftotext/`
- **Base URL:** `https://selectpdf.com/api2`
- **Official documentation:** [Search PDF File](https://selectpdf.com/pdf-to-text-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The PDF file to search. |
| `search_text` | body | `string` | yes | Text to search for inside the PDF. |
