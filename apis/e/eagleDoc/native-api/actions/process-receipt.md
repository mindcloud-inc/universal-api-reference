# Process Receipt with Eagle Doc

Creates a receipt extraction in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/receipt/v3/processing`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Process Receipt](https://www.eagle-doc.com/en/documentation/receipt-ocr/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Receipt file to upload |
| `fullText` | query | `boolean` | no | Include the extracted full text by page |
| `polygon` | query | `boolean` | no | Include polygon coordinates in the response |
| `privacy` | query | `boolean` | no | Whether Eagle Doc should avoid storing the uploaded file |
| `speed` | query | `boolean` | no | Prefer faster processing over higher accuracy |
