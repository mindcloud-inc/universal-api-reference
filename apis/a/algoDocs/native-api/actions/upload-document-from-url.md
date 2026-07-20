# Upload Document From URL with AlgoDocs

Creates a document in AlgoDocs from a public URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/upload_url/:extractorId/:folderId`
- **Base URL:** `https://api.algodocs.com/v1`
- **Official documentation:** [Upload Document From URL](https://api.algodocs.com/#documents)

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
| `url` | body | `string` | yes | A publicly available URL for the file to upload. |
