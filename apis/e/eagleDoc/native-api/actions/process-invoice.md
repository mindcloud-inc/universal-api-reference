# Process Invoice with Eagle Doc

Creates an invoice extraction in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/invoice/v1/processing`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Process Invoice](https://www.eagle-doc.com/en/documentation/invoice-ocr/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Invoice file to upload |
| `fullText` | query | `boolean` | no | Include the extracted full text by page |
| `polygon` | query | `boolean` | no | Include polygon coordinates in the response |
| `privacy` | query | `boolean` | no | Whether Eagle Doc should avoid storing the uploaded file |
| `signature` | query | `boolean` | no | Extract signature data from the invoice |
