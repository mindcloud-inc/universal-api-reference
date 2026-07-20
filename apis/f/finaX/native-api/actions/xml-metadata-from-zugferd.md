# XML Metadata From ZUGFeRD with finaX

Retrieves XML metadata from a ZUGFeRD PDF in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pdf/metadata/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [XML Metadata From ZUGFeRD](https://docs.finax.dev/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | ZUGFeRD invoice file. |
