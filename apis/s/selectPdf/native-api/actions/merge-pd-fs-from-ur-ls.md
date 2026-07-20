# Merge PDFs from URLs with SelectPdf

## Endpoint

- **Method:** `POST`
- **Path:** `/pdfmerge/`
- **Base URL:** `https://selectpdf.com/api2`
- **Official documentation:** [Merge PDFs from URLs](https://selectpdf.com/pdf-merge-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url_1` | body | `string` | yes | The first public PDF URL to merge. |
| `url_2` | body | `string` | yes | The second public PDF URL to merge. |
