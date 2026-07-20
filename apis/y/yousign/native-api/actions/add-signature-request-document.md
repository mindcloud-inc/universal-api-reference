# Add Signature Request Document with Yousign

Adds a document to a Yousign signature request.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_requests/:signatureRequestId/documents`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Add Signature Request Document](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-documents-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
| `file` | body | `file` | yes | Binary file to upload. |
| `nature` | body | `string` | yes | Document nature. |
| `name` | body | `string` | no | Optional document name. |
| `password` | body | `string` | no | Password for protected files, when needed. |
| `parse_anchors` | body | `boolean` | no | Automatically parse smart anchors. |
| `insert_after_id` | body | `string` | no | Insert after an existing document ID. |
