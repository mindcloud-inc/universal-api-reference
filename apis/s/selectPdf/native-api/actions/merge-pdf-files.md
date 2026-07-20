# Merge PDF Files with SelectPdf

## Endpoint

- **Method:** `POST`
- **Path:** `/pdfmerge/`
- **Base URL:** `https://selectpdf.com/api2`
- **Official documentation:** [Merge PDF Files](https://selectpdf.com/pdf-merge-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_1` | body | `file` | yes | The first PDF file to merge. |
| `file_2` | body | `file` | yes | The second PDF file to merge. |
