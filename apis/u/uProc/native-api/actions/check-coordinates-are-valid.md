# Check Coordinates Are Valid with UProc

## Endpoint

- **Method:** `POST`
- **Path:** `/process`
- **Base URL:** `https://api.uproc.io/api/v2`
- **Official documentation:** [Check Coordinates Are Valid](https://docs.uproc.io/api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.coordinates` | body | `string` | yes | Latitude and longitude pair to validate. |
