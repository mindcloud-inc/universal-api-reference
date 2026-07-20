# Parse Driving License with Eagle Doc

Creates a driving license extraction in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/anydoc/v1/processing`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Parse Driving License](https://www.eagle-doc.com/en/documentation/anydoc-ocr/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Driving license file to upload |
