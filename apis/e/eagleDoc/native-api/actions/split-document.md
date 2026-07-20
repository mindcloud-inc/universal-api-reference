# Split Document with Eagle Doc

Creates document split segments in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/doc/v1/split`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Split Document](https://www.eagle-doc.com/en/documentation/anydoc-split/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document file to split |
