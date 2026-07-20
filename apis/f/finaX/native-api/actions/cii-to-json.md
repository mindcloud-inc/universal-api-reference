# CII To JSON with finaX

Retrieves invoice JSON from CII XML in finaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/json/cii/`
- **Base URL:** `https://api.finax.dev`
- **Official documentation:** [CII To JSON](https://docs.finax.dev/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `xml` | body | `string` | yes | CII XML payload. |
