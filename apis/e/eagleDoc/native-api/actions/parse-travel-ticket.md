# Parse Travel Ticket with Eagle Doc

Creates a travel ticket extraction in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/anydoc/v1/processing`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Parse Travel Ticket](https://www.eagle-doc.com/en/documentation/anydoc-ocr/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Travel ticket file to upload |
