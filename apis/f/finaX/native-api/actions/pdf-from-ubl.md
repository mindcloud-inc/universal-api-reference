# PDF From UBL with finaX

Creates a ZUGFeRD PDF from UBL XML in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pdf/ubl/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [PDF From UBL](https://docs.finax.dev/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `xml` | body | `string` | yes | UBL XML payload. |
