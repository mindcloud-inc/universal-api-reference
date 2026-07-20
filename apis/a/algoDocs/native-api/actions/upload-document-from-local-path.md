# Upload Document From Local Path with AlgoDocs

Creates a document in AlgoDocs from a local file.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/upload_local/:extractorId/:folderId`
- **Base URL:** `https://api.algodocs.com/v1`
- **Official documentation:** [Upload Document From Local Path](https://api.algodocs.com/#documents)

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
| `file` | body | `file` | yes | The local file path or file payload for the document upload. |
