# Get Coordinates by Search with UProc

## Endpoint

- **Method:** `POST`
- **Path:** `/process`
- **Base URL:** `https://api.uproc.io/api/v2`
- **Official documentation:** [Get Coordinates by Search](https://docs.uproc.io/api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.address` | body | `string` | yes | Address or place text to geocode. |
