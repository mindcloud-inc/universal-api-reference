# PDF From CII with finaX

Creates a ZUGFeRD PDF from CII XML in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pdf/cii/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [PDF From CII](https://docs.finax.dev/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `xml` | body | `string` | yes | CII XML payload. |
