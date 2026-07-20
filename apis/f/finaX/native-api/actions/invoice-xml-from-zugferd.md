# Invoice XML From ZUGFeRD with finaX

Retrieves invoice XML from a ZUGFeRD PDF in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pdf/xml/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [Invoice XML From ZUGFeRD](https://docs.finax.dev/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | ZUGFeRD invoice file. |
