# Process Finance Document with Eagle Doc

Creates a finance document extraction in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/finance/v1/processing`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Process Finance Document](https://www.eagle-doc.com/en/documentation/finance-ocr/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Receipt or invoice file to upload |
| `fullText` | query | `boolean` | no | Include the extracted full text by page |
| `polygon` | query | `boolean` | no | Include polygon coordinates in the response |
| `privacy` | query | `boolean` | no | Whether Eagle Doc should avoid storing the uploaded file |
| `signature` | query | `boolean` | no | Extract signature data from the finance document |
