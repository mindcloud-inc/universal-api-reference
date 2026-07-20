# Get Document Data with GIRITON

Retrieves data for a specific GIRITON document.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentId/data`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [Get Document Data](https://rest.giriton.com/apidoc/#/Documents/getDocumentData)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Document ID. |
