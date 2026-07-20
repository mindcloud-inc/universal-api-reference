# Check Credit Card Checksum with UProc

## Endpoint

- **Method:** `POST`
- **Path:** `/process`
- **Base URL:** `https://api.uproc.io/api/v2`
- **Official documentation:** [Check Credit Card Checksum](https://docs.uproc.io/api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.credit_card` | body | `string` | yes | Credit card number to validate. |
