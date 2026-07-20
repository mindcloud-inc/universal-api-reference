# Upload Document For Processing with Nanonets OCR

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/:workflow_id/documents`
- **Base URL:** `https://app.nanonets.com/api/v4`
- **Official documentation:** [Upload Document For Processing](https://apidocs.nanonets.com/docs/api/document-processing/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `list` | yes | Workflow identifier. |
| `file` | body | `file` | yes | Document file to upload for processing. A public file URL can also be used for runtime testing via MindCloud's file handling. |
| `async` | body | `boolean` | no | Whether to process the document asynchronously. |
| `metadata` | body | `string` | no | Optional metadata attached to the document. Use a JSON string when passing structured metadata. |
