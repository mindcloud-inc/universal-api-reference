# Get Advanced Speech by Text with UProc

## Endpoint

- **Method:** `POST`
- **Path:** `/process`
- **Base URL:** `https://api.uproc.io/api/v2`
- **Official documentation:** [Get Advanced Speech by Text](https://docs.uproc.io/api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.gender` | body | `string` | yes | Voice gender. |
| `params.language` | body | `string` | yes | Voice language or accent. |
| `params.text` | body | `string` | yes | Text to convert into speech. |
