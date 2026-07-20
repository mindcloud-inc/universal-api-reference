# Get ASIN by EAN with UProc

## Endpoint

- **Method:** `POST`
- **Path:** `/process`
- **Base URL:** `https://api.uproc.io/api/v2`
- **Official documentation:** [Get ASIN by EAN](https://docs.uproc.io/api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.ean` | body | `string` | yes | EAN code to convert into an ASIN. |
