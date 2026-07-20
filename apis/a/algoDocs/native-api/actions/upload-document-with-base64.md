# Upload Document With Base64 with AlgoDocs

Creates a document in AlgoDocs from base64 content.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/upload_base64/:extractorId/:folderId`
- **Base URL:** `https://api.algodocs.com/v1`
- **Official documentation:** [Upload Document With Base64](https://api.algodocs.com/#documents)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractorId` | path | `string` | yes | The extractor ID from your AlgoDocs account. |
| `folderId` | path | `string` | yes | The folder ID where the uploaded document should be saved. |
| `file_base64` | body | `string` | yes | The base64-encoded file contents. |
| `filename` | body | `string` | yes | The file name to associate with the uploaded base64 document. |
