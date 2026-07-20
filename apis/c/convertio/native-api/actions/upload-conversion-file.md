# Upload Conversion File with Convertio

Uploads a file for a conversion in Convertio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/convert/:id/:filename`
- **Base URL:** `https://api.convertio.co`
- **Official documentation:** [Upload Conversion File](https://developers.convertio.co/api/docs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | path | `string` | yes | Input filename including extension. |
| `id` | path | `string` | yes | Conversion ID returned by Start Conversion. |
| `file` | body | `file` | yes | Binary file contents to upload for the conversion. |
