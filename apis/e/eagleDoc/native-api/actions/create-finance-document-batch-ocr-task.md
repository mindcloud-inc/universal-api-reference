# Create Finance Document Batch OCR Task with Eagle Doc

Creates a finance document batch OCR task in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/finance/extract/batch/task/v1`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Create Finance Document Batch OCR Task](https://www.eagle-doc.com/en/documentation/batch-ocr/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docType` | query | `string` | no | Document type used for finance batch extraction |
| `file` | body | `file` | yes | Archive file that contains the finance batch input files |
| `fullText` | query | `boolean` | no | Include the extracted full text by page for each result |
| `polygon` | query | `boolean` | no | Include polygon coordinates in each extracted result |
| `privacy` | query | `boolean` | no | Whether Eagle Doc should avoid storing the uploaded file |
