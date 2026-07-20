# Upload CSV File with SeekTable

Uploads a CSV file to a SeekTable cube.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cube/import/csv`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Upload CSV File](https://www.seektable.com/help/web-api-integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cubeId` | query | `string` | no | GUID of an existing CSV cube to refresh. If not specified a new cube is created. |
| `filename` | query | `string` | no | Explicitly specified name of the CSV file. Useful when CSV content goes directly in the request body. |
| `file` | body | `file` | yes | CSV file content uploaded as multipart/form-data file. |
