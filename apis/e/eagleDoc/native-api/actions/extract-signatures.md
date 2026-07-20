# Extract Signatures with Eagle Doc

Creates a signature extraction in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/signature/v1/extract`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Extract Signatures](https://www.eagle-doc.com/en/documentation/signature-extraction/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document file that contains signatures |
