# Extract Receipt Data From File with WiseOCR

Retrieves extracted receipt data from WiseOCR using an uploaded file.

## Endpoint

- **Method:** `POST`
- **Path:** `/file`
- **Base URL:** `https://api.wiseocr.com/v1`
- **Official documentation:** [Extract Receipt Data From File](https://developers.wiseocr.com/file-data-extraction)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Receipt image or PDF file |
| `skipItems` | body | `boolean` | no | Skip detailed line item extraction to speed up processing |
