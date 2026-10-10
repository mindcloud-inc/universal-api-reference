# Upload Document with PestPac

## Endpoint

- **Method:** `POST`
- **Path:** `Documents/:documentId/upload`
- **Base URL:** `https://api.workwave.com/pestpac/v1/`
- **Official documentation:** [Upload Document](https://developer.workwave.com/documentation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | Document ID returned by Create Document. |
| `file` | body | `file` | yes | One file to upload as multipart/form-data. PestPac supports one file per Document ID. |
